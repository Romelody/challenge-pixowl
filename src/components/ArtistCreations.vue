<template>
  <div id="artist-creations">
    <div class="container padding-y">
      <h2>What our Artists are creating</h2>
      <ArtistCreation />
    </div>
  </div>
</template>
<script>
import ArtistCreation from "./mini-components/ArtistCreation";
export default {
  components: {
    ArtistCreation
  }
};
</script>
<style lang="scss" scoped>
#artist-creations {
  background: $dark-grey;
  padding: 40px 0;
}
</style>
