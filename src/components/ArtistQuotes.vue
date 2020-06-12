<template>
  <div id="artist-quotes">
    <div class="container padding-y">
      <h2>Quotes from voxel artists</h2>
      <div :class="tabletView ? 'quotes-container-tablet' : 'quotes-container'">
        <ArtistQuote
          v-for="artistQuote in artistQuotes"
          :key="artistQuote.id"
          :textQuote="artistQuote.textQuote"
          :artistName="artistQuote.artistName"
          :artistJob="artistQuote.artistJob"
          :avatarPosition="artistQuote.avatarPosition"
          :backgroundColor="artistQuote.backgroundColor"
          :imgArtist="artistQuote.imgArtist"
          :tabletView="tabletView"
        />
      </div>
    </div>
  </div>
</template>
<script>
import ArtistQuote from "./mini-components/ArtistQuote";
import imageArtistWilliam from "../assets/img/quote-william.png";
import imageArtistAlex from "../assets/img/quote-alex.png";
import imageArtistZach from "../assets/img/quote-zach.png";
import imageArtistNicolas from "../assets/img/quote-nicolas.png";
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
            '"VoxEdit has impressed me, since it\'s the fusion of a modeling editor with an animation system all in the same software."',
          artistName: "William Santacruz",
          artistJob: "Professional Voxel Artist",
          avatarPosition: "left",
          backgroundColor: "#282E36",
          imgArtist: imageArtistWilliam
        },
        {
          id: 1,
          textQuote:
            '"VoxEdit is a game changer for voxel artists looking to animatie, being the only dedicated voxel editor that features skeletal rigging and timeline animation."',
          artistName: "Alex Florezz",
          artistJob: "Professional Voxel Artist",
          avatarPosition: "right",
          backgroundColor: "#2F3740",
          imgArtist: imageArtistAlex
        },
        {
          id: 2,
          textQuote:
            '"It shows some excellent promise in the direction it\'s going with a dedicated team. Adding a full functioning animation system within the editor makes it stand out from the rest!"',
          artistName: "Zach Soares",
          artistJob: "Professional Voxel",
          avatarPosition: "left",
          backgroundColor: this.tabletView ? "#282E36" : "#2F3740",
          imgArtist: imageArtistZach
        },
        {
          id: 3,
          textQuote:
            '"One of the easier tool to create animations in voxel art, with an attractive and a very simple easy-to-use interface for beginners."',
          artistName: "Nicolas Morrone",
          artistJob: "Professional Voxel",
          avatarPosition: "right",
          backgroundColor: this.tabletView ? "#2F3740" : "#282E36",
          imgArtist: imageArtistNicolas
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
  .quotes-container-tablet {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 0 32px;
  }
}
</style>
