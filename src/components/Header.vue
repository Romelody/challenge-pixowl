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
        <div class="languaje">
          <img src="../assets/img/en-flag.png" alt="" />
          <p>EN</p>
          <img src="../assets/img/arrow-dropdown.svg" alt="" />
        </div>
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
    .languaje {
      cursor: pointer;
      display: flex;
      flex-direction: row;
      background: #3b4148;
      padding: 10px 0;
      border-radius: 15px;
      p {
        font-weight: 600;
      }
      img {
        padding: 0 10px;
      }
    }
  }
  ul {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  a {
    font-weight: 600;
    color: $light-gray;
    padding-right: 20px;
  }
}
</style>
