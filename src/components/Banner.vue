<template>
  <div id="banner">
    <div class="container">
      <div class="textoBanner">
        <h1>VoxEdit Beta</h1>
        <p>
          The first software that allows you to create your own voxel models,
          rig them, and animate them in no time.
        </p>
        <a href="#" class="btn">Download now!</a>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
#banner {
  background-image: url(../assets/img/banner.png);
  background-size: cover;
  width: 100%;
  height: 480px;
}
.textoBanner {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  width: 50%;
  color: $white;

  h1 {
    font-size: 50px;
    margin-bottom: 18px;
  }
  p {
    font-size: 20px;
    margin-bottom: 30px;
  }
  .btn {
    background: $blue;
    color: $white;
    font-size: 25px;
    text-align: center;
    width: 250px;
    padding: 10px;
    border-radius: 25px;
  }
}
</style>
