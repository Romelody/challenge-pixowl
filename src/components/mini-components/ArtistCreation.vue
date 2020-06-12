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
        <p class="nickname" v-if="tabletView">75/300</p>
        <p class="nickname" v-else>{{ textArt }}</p>
        <div class="money" v-if="tabletView">
          <img src="@/assets/img/sand-icon.svg" />
          <p>700</p>
        </div>
        <div
          :class="tabletView ? 'more-artist-info-tablet' : 'more-artist-info'"
        >
          <img src="@/assets/img/add.svg" alt="" />
        </div>
      </div>
      <div class="runner" v-if="tabletView"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ArtistCreation",
  props: {
    titleArt: String,
    textArt: String,
    imgArt: String,
    tabletView: Boolean
  }
};
</script>
<style lang="scss" scoped>
#artistCreation {
  .art-card {
    width: 200px;
    position: relative;
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
        color: $light-grey;
        font-size: 15px;
      }
    }
    .money {
      position: absolute;
      display: flex;
      justify-content: space-between;
      width: 35%;
      align-items: center;
      bottom: 8px;
      left: 8px;
      p {
        color: $yellow;
        font-size: 20px;
        font-weight: 600;
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
      border: 1px solid $art-light-grey;
    }
    .more-artist-info-tablet {
      position: absolute;
      display: flex;
      justify-content: center;
      align-items: center;
      bottom: 8px;
      right: 8px;
      width: 42px;
      height: 42px;
      border-radius: 25px;
      background: $grey-add;
    }
    .runner {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background: $medium-grey;
      position: absolute;
      top: 10px;
      left: 10px;
    }
  }
}
</style>
