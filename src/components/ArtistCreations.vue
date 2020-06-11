<template>
  <div id="artist-creations">
    <div class="container padding-y">
      <h2>What our Artists are creating</h2>
      <div class="creation-container">
        <ArtistCreation
          v-for="artistCreation in artistCreations"
          :key="artistCreation.id"
          :titleArt="artistCreation.titleArt"
          :textArt="artistCreation.textArt"
          :imgArt="artistCreation.imgArt"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ArtistCreation from "./mini-components/ArtistCreation";
import imageWilliam from "@/assets/img/art-william.png";
import imageNicolas from "@/assets/img/art-nicolas.png";
import imageBenjiro from "@/assets/img/art-benjiro.png";
import imageAgustin from "@/assets/img/art-agustin.png";

export default {
  components: {
    ArtistCreation
  },
  data() {
    return {
      artistCreations: [
        {
          id: 0,
          titleArt: "FLYING ALIEN",
          textArt: "@william",
          imgArt: imageWilliam
        },
        {
          id: 1,
          titleArt: "DINO STORE",
          textArt: "@nicolas",
          imgArt: imageNicolas
        },
        {
          id: 1,
          titleArt: "MEDIEVAL WELL",
          textArt: "@benjiro",
          imgArt: imageBenjiro
        },
        {
          id: 1,
          titleArt: "SAMURAI BRIDGE",
          textArt: "@agustin",
          imgArt: imageAgustin
        },
        {
          id: 1,
          titleArt: "FLYING ALIEN",
          textArt: "@william",
          imgArt: imageWilliam
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
#artist-creations {
  background: $dark-grey;
  padding: 40px 0;
  .creation-container {
    display: flex;
    justify-content: space-between;
  }
}
</style>
