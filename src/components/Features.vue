<template>
  <div id="features">
    <div class="container">
      <div>
        <h2>VoxEdit features</h2>
        <Feature />
      </div>
    </div>
  </div>
</template>
<script>
import Feature from "./mini-components/Feature";
export default {
  components: {
    Feature
  }
};
</script>

<style lang="scss" scoped>
#features {
  background: $medium-grey;
  padding: 40px 0;
  h2 {
    color: $white;
    font-size: 30px;
    display: flex;
    justify-content: center;
  }
}
</style>
