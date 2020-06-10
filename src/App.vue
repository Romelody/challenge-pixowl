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
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
}
a {
  text-decoration: none;
}

ul li {
  list-style: none;
}
h2 {
  color: $white;
  font-size: 40px;
  font-weight: 800;
  display: flex;
  justify-content: center;
  padding-bottom: 20px;
}
.container {
  width: 90%;
  height: 100%;
  margin: 0 auto;
}
.padding-y {
  padding: 90px 0;
}
</style>
