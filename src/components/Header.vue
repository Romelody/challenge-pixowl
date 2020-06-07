<template>
  <div id="header">
    <div class="container">
      <div class="header">
        <ul>
          <li>
            <a href="#"> <img src="../assets/Vox-Logo.svg" alt=""/></a>
          </li>
          <li><a href="#">Features</a></li>
          <li><a href="#">Download</a></li>
          <li><a href="#">Creator Fund</a></li>
          <li><a href="#">FAQs</a></li>
          <li><a href="#">Feedback</a></li>
        </ul>
        <span>EN</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#header {
  background: $black;
  color: $light-gray;
  .header {
    padding: 15px 0;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  ul {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  a {
    color: $light-gray;
    padding-right: 20px;
  }
}
</style>
