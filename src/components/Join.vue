<template>
  <div id="join">
    <div class="container content">
      <h2>JOIN OUR COMMUNITY</h2>
      <p class="subtitle">
        Be part of our amazing community and stay<br />tuned for the news.
      </p>
      <a class="btn-join">JOIN US</a>
    </div>
    <img src="../assets/img/join-background.png" alt="" />
  </div>
</template>
<style lang="scss" scoped>
#join {
  display: flex;
  justify-content: center;
  height: 100%;
  padding: 20px 0;
  background: $black;
  position: relative;
  .content {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  img {
    position: absolute;
    left: 70px;
    top: 0;
    height: 100%;
  }
  .subtitle {
    text-align: center;
    color: $light-grey;
    font-size: 20px;
    padding-bottom: 20px;
  }
  .btn-join {
    width: 200px;
    display: flex;
    justify-content: center;
    background: transparent linear-gradient(1deg, #a134ff 0%, #6271fe 100%) 0%
      0% no-repeat padding-box;
    text-transform: uppercase;
    color: $white;
    padding: 10px;
    border-radius: 35px;
  }
}
</style>
