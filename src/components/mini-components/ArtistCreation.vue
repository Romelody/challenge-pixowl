<template>
  <div id="artistCreation">
    <div class="art-card">
      <div class="art-img">
        <img :src="imgArt" alt="" />
      </div>
      <div class="artist-info">
        <h3>
          <strong>{{ titleArt }}</strong>
        </h3>
        <p class="nickname">{{ textArt }}</p>
        <div class="more-artist-info">
          <img src="@/assets/img/add.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ArtistCreation",
  props: {
    titleArt: String,
    textArt: String,
    imgArt: String
  }
};
</script>
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
    }
    .artist-info {
      position: relative;
      width: 200px;
      height: 170px;
      padding: 4px 0 0 8px;
      background: $medium-grey;
      border-radius: 0 0 10px 10px;
      text-align: left;
      color: $white;
      height: 90px;
      h3 strong {
        font-weight: 600;
        text-transform: uppercase;
        font-size: 18px;
      }
      p {
        color: $light-gray;
        font-size: 15px;
      }
    }
    .more-artist-info {
      position: absolute;
      display: flex;
      justify-content: center;
      align-items: center;
      bottom: 8px;
      right: 8px;
      width: 30px;
      height: 30px;
      border-radius: 25px;
      background: $grey-add;
      border: 1px solid $light-gray;
    }
  }
}
</style>
