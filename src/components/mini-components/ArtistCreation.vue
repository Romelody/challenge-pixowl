<template>
  <div id="artistCreation">
    <div class="art-card">
      <div class="art-img">
        <img src="../../assets/img/art-william.png" alt="" />
      </div>
      <div class="artist-info">
        <h3>
          <strong>{{ titleFeature }}FLYING ALIEN</strong>
        </h3>
        <p class="nickname">{{ textFeature }}@william</p>
        <div class="more-artist-info"></div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
#artistCreation {
  .art-card {
    width: 200px;
    .art-img {
      width: 200px;
      height: 170px;
      padding: 15px;
      background: $art-light-grey;
      border-radius: 10px 10px 0 0;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      img {
        width: 120px;
        height: 116px;
      }
    }
    .artist-info {
      width: 200px;
      height: 170px;
      padding: 15px;
      background: $medium-grey;
      border-radius: 0 0 10px 10px;
      text-align: left;
      color: $white;
      height: 90px;
      h3 {
        font-size: SemiBold;
        text-transform: uppercase;
        font-size: 18px;
      }
      p {
        color: $light-gray;
        font-size: 15px;
      }
    }
    .more-artist-info {
      width: 25px;
      height: 25px;
      border-radius: 25px;
      background: $dark-grey;
      border: 1px solid $light-gray;
      right: 3px;
    }
  }
}
</style>
