<template>
  <div
    id="feature"
    :style="{ backgroundImage: `url(${bgImage})` }"
    :class="tabletView ? 'background-image-tablet' : 'background-image'"
  >
    <div :class="tabletView ? 'text-component-tablet' : 'text-component'">
      <h3>
        {{ titleFeature }}
      </h3>
      <p>
        {{ textFeature }}
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Feature",
  props: {
    titleFeature: String,
    textFeature: String,
    bgImage: String,
    tabletView: Boolean
  }
};
</script>
<style lang="scss" scoped>
.background-image-tablet {
  width: 650px;
  height: 360px;
}
.background-image {
  width: 400px;
  height: 410px;
}
#feature {
  background-repeat: no-repeat;
  background-size: cover;
  margin-bottom: 40px;

  .text-component {
    padding: 40px;
    color: $white;
    h3 {
      font-size: 25px;
      font-weight: 700;
      text-align: center;
      margin-bottom: 15px;
    }
    p {
      font-size: 15px;
      text-align: center;
      letter-spacing: 0px;
      color: $light-grey;
    }
  }
  .text-component-tablet {
    padding: 46px 0 0 38px;
    color: $white;
    h3 {
      font-size: 25px;
      font-weight: 700;
      margin-bottom: 15px;
    }
    p {
      font-size: 20px;
      letter-spacing: 0px;
      color: $light-grey;
      width: 40%;
    }
  }
}
</style>
