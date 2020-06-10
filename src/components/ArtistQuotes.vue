<template>
  <div id="artist-quotes">
    <div class="container padding-y">
      <h2>Quotes from voxel artists</h2>
      <ArtistQuote />
    </div>
  </div>
</template>
<script>
import ArtistQuote from "./mini-components/ArtistQuote";
export default {
  components: {
    ArtistQuote
  }
};
</script>
<style lang="scss" scoped>
#artist-quotes {
  background: $medium-grey;
  h2 {
    color: $white;
    font-size: 30px;
    display: flex;
    justify-content: center;
    padding-bottom: 20px;
  }
}
</style>
