<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from "./views/Home.vue";

export default {
  name: "App",
  components: {
    Home
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
}

ul li {
  list-style: none;
}

.container {
  width: 90%;
  height: 100%;
  margin: 0 auto;
}
</style>
