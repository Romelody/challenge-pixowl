<template>
  <div id="artist-quote">
    <div class="content">
      <div class="quote">
        <div
          class="artist-art"
          :class="
            avatarPosition === 'right' ? 'right-direction' : 'left-direction'
          "
        >
          <img src="../../assets/img/quote-william.png" alt="" />
          <div class="diamond"></div>
        </div>
        <div
          class="artist-quote"
          :class="avatarPosition === 'right' ? 'right-padding' : 'left-padding'"
          :style="{ background: backgroundColor }"
        >
          <p class="text">
            {{ textQuote }}
          </p>
          <p class="professional">
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
    backgroundColor: String
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
    left: 0;
  }
  .right-direction {
    right: 0;
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
      /* background: $dark-grey; */
      border-radius: 10px;
      box-shadow: 0px 3px 6px #00000029;
      color: $white;
      .text {
        padding-bottom: 15px;
      }
    }
    .right-padding {
      margin-right: 73px;
      padding: 32px 120px 32px 20px;
    }
    .left-padding {
      margin-left: 73px;
      padding: 32px 60px 32px 80px;
    }
    .professional {
      color: $light-grey;
    }
    .artist-name {
      color: $blue;
      font-family: bold;
    }
  }
}
</style>
