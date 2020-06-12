<template>
  <div id="artist-quote">
    <div class="content">
      <div class="quote">
        <div
          class="artist-art"
          :class="[
            avatarPosition === 'right' ? 'right-direction' : 'left-direction',
            { 'avatar-top': tabletView }
          ]"
        >
          <img :src="imgArtist" alt="" />
          <div class="diamond"></div>
        </div>
        <div
          :class="[
            tabletView ? 'artist-quote-tablet' : 'artist-quote',
            avatarPosition === 'right' ? 'right-padding' : 'left-padding'
          ]"
          :style="{ background: backgroundColor }"
        >
          <p :class="avatarPosition === 'right' ? 'text-align' : 'text'">
            {{ textQuote }}
          </p>
          <p
            class="professional"
            :class="{
              'professional-no-align': avatarPosition === 'left' && !tabletView
            }"
          >
            <span class="artist-name">{{ artistName }}</span> - {{ artistJob }}
            Artist
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ArtistQuote",
  props: {
    textQuote: String,
    artistName: String,
    artistJob: String,
    avatarPosition: String,
    backgroundColor: String,
    imgArtist: String,
    tabletView: Boolean
  }
};
</script>

<style lang="scss" scoped>
#artist-quote {
  background: $medium-grey;
  padding: 16px 0;
  margin: 20px 0;
  .content {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    position: relative;
  }
  .artist-art {
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 3;
    img {
      z-index: 3;
      position: absolute;
    }
  }
  .left-direction {
    left: 30px;
  }
  .right-direction {
    right: 30px;
  }
  .avatar-top {
    top: 10px;
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
    width: 99%;
    .artist-quote {
      display: flex;
      flex-direction: column;
      justify-content: center;
      height: 160px;
      border-radius: 10px;
      box-shadow: 0px 3px 6px #00000029;
      color: $white;
      .text {
        padding-bottom: 15px;
        padding-left: 34px;
        font-size: 15px;
        width: 90%;
      }
      .text-align {
        padding-bottom: 15px;
        font-size: 15px;
        width: 90%;
      }
    }
    .artist-quote-tablet {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 240px;
      border-radius: 10px;
      box-shadow: 0px 3px 6px #00000029;
      color: $white;
      .text {
        padding-bottom: 15px;
        padding-left: 40px;
        font-size: 20px;
        width: 80%;
      }
      .text-align {
        padding-bottom: 15px;
        font-size: 20px;
        width: 80%;
      }
    }
    .right-padding {
      margin-right: 73px;
      padding: 32px 120px 32px 20px;
    }
    .left-padding {
      margin-left: 73px;
      padding: 32px 6px 32px 80px;
    }
    .professional {
      color: $light-grey;
    }
    .professional-no-align {
      padding-left: 34px;
    }
    .artist-name {
      color: $blue;
      font-weight: 600;
    }
  }
}
</style>
