<template>
  <div id="artist-quote">
    <div class="content">
      <div class="quote">
        <div class="artist-art">
          <img src="../../assets/img/quote-william.png" alt="" />
          <div class="diamond"></div>
        </div>
        <div class="artist-quote">
          <p class="text">
            "VoxEdit has impressed me, since it's the fusion of a modeling
            editor with an animation system all in the same software."
          </p>
          <p class="professional">
            <span class="artist-name">Zach Soares</span> - Professional Voxel
            Artist
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
#artist-quote {
  background: $medium-grey;
  padding: 40px 0;
  margin: 20px 0;
  width: 50%;
  .content {
    display: flex;
    flex-direction: row;
    align-items: center;
    position: relative;
  }
  .artist-art {
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 3;
    left: 0;
    img {
      z-index: 3;
      position: absolute;
    }
  }
  .diamond {
    background: $dark-grey;
    width: 130px;
    height: 130px;
    transform: rotate(45deg);
    border-radius: 10px;
    top: 0;
    z-index: 0;
  }

  .quote {
    top: 0;
    display: flex;
    flex-direction: row;
    align-items: center;
    .artist-quote {
      margin-left: 80px;
      padding: 20px 60px 20px 80px;
      background: $dark-grey;
      border-radius: 10px;
      box-shadow: 0px 3px 6px #00000029;
      color: $white;
      .text {
        padding-bottom: 15px;
      }
    }
    .professional {
      color: $light-gray;
    }
    .artist-name {
      color: $blue;
      font-family: bold;
    }
  }
}
</style>
