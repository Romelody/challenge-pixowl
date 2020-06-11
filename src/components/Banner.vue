<template>
  <div
    id="banner"
    :class="tabletView ? 'banner-container-tablet' : 'banner-container'"
  >
    <div class="container">
      <div :class="tabletView ? 'textoBanner-tablet' : 'textoBanner'">
        <h1>VoxEdit Beta</h1>
        <p>
          The first software that allows you to create your own voxel models,
          rig them, and animate them in no time.
        </p>
        <a href="#" class="btn" v-if="!tabletView">Download now!</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tabletView: Boolean
  }
};
</script>

<style lang="scss" scoped>
.banner-container {
  background-image: url(../assets/img/banner.png);
  height: 480px;
}
.banner-container-tablet {
  background-image: url(../assets/img/banner-tablet.png);
  height: 1010px;
}
#banner {
  background-size: cover;
  width: 100%;
}
.textoBanner {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  width: 50%;
  color: $white;
  font-family: "montserratRegular";

  h1 {
    font-size: 50px;
    margin-bottom: 18px;
    font-weight: 700;
  }
  p {
    font-size: 20px;
    margin-bottom: 30px;
  }
  .btn {
    background: $blue;
    color: $white;
    font-size: 22px;
    text-align: center;
    width: 250px;
    padding: 10px;
    border-radius: 25px;
    font-weight: 700;
  }
}
.textoBanner-tablet {
  display: flex;
  flex-direction: column;
  height: 100%;
  width: 79%;
  color: $white;
  font-family: "montserratRegular";
  padding: 80px 0 0 50px;
  h1 {
    font-size: 50px;
    margin-bottom: 18px;
    font-weight: 700;
  }
  p {
    font-size: 20px;
    margin-bottom: 30px;
  }
  .btn {
    background: $blue;
    color: $white;
    font-size: 22px;
    text-align: center;
    width: 250px;
    padding: 10px;
    border-radius: 25px;
    font-weight: 700;
  }
}
</style>
