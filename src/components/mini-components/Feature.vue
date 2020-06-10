<template>
  <div id="feature" :style="{ backgroundImage: `url(${bgImage})` }">
    <div class="text-component">
      <h3>
        <strong>{{ titleFeature }}</strong>
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
    bgImage: String
  }
};
</script>
<style lang="scss" scoped>
#feature {
  background-repeat: no-repeat;
  background-size: 400px 410px;
  width: 400px;
  height: 410px;
  .text-component {
    padding: 40px;
    color: $white;
    h3 {
      font-weight: 500;
      text-align: center;
      margin-bottom: 15px;
      strong {
      }
    }
    p {
      text-align: center;
      letter-spacing: 0px;
    }
  }
}
</style>
