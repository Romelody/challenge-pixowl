<template>
  <div id="artist-creations">
    <div class="container">
      <h2>Artist Creations</h2>
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
  h2 {
    color: $white;
    font-size: 30px;
    display: flex;
    justify-content: center;
    padding-bottom: 20px;
  }
}
</style>
