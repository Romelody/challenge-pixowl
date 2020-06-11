<template>
  <div id="artist-quotes">
    <div class="container padding-y">
      <h2>Quotes from voxel artists</h2>
      <div class="quotes-container">
        <ArtistQuote
          v-for="artistQuote in artistQuotes"
          :key="artistQuote.id"
          :textQuote="artistQuote.textQuote"
          :artistName="artistQuote.artistName"
          :artistJob="artistQuote.artistJob"
          :avatarPosition="artistQuote.avatarPosition"
          :backgroundColor="artistQuote.backgroundColor"
        />
      </div>
    </div>
  </div>
</template>
<script>
import ArtistQuote from "./mini-components/ArtistQuote";
export default {
  components: {
    ArtistQuote
  },
  data() {
    return {
      artistQuotes: [
        {
          id: 0,
          textQuote:
            "VoxEdit has impressed me, since it's the fusion of a modeling editor with an animation system all in the same software.",
          artistName: "Zach Soares",
          artistJob: "Professional Voxel",
          avatarPosition: "left",
          backgroundColor: "#282E36"
        },
        {
          id: 1,
          textQuote:
            "VoxEdit has impressed me, since it's the fusion of a modeling editor with an animation system all in the same software.",
          artistName: "Zach Soares",
          artistJob: "Professional Voxel",
          avatarPosition: "right",
          backgroundColor: "#2F3740"
        },
        {
          id: 2,
          textQuote:
            "VoxEdit has impressed me, since it's the fusion of a modeling editor with an animation system all in the same software.",
          artistName: "Zach Soares",
          artistJob: "Professional Voxel",
          avatarPosition: "left",
          backgroundColor: "#2F3740"
        },
        {
          id: 3,
          textQuote:
            "VoxEdit has impressed me, since it's the fusion of a modeling editor with an animation system all in the same software.",
          artistName: "Zach Soares",
          artistJob: "Professional Voxel",
          avatarPosition: "right",
          backgroundColor: "#282E36"
        }
      ]
    };
  },
  props: {
    tabletView: Boolean
  }
};
</script>
<style lang="scss" scoped>
#artist-quotes {
  background: $medium-grey;
  .quotes-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 0 32px;
  }
}
</style>
