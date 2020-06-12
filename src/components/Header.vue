<template>
  <div id="header">
    <div class="container">
      <div v-if="!tabletView" class="header">
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
          <img src="../assets/img/en-flag.png" alt="En" />
          <p>EN</p>
          <img src="../assets/img/arrow-dropdown.svg" alt="arrowDrop" />
        </div>
      </div>

      <div v-if="tabletView || (!tabletView && clicked)" class="header">
        <a href="#"> <img src="../assets/Vox-Logo.svg" alt=""/></a>
        <div class="arrow-drop">
          <div class="languaje">
            <img src="../assets/img/en-flag.png" alt="En" />
            <p>EN</p>
            <img src="../assets/img/arrow-dropdown.svg" alt="arrowDrop" />
          </div>
          <div
            class="navIcon"
            v-if="tabletView && !clicked"
            @click="clicked = !clicked"
          >
            <img src="../assets/img/burger.svg" class="burger" alt="burger" />
          </div>
          <div class="burger-content" v-if="tabletView && clicked">
            <ul
              :class="{
                'tablet-nav-links': tabletView,
                'nav-links': !tabletView
              }"
              v-if="clicked || !tabletView"
            >
              <li><a href="#">Features</a></li>
              <li><a href="#">Download</a></li>
              <li><a href="#">Creator Fund</a></li>
              <li><a href="#">FAQs</a></li>
              <li><a href="#">Feedback</a></li>
            </ul>
            <div
              @click="clicked = !clicked"
              class="close"
              v-if="tabletView && clicked"
            >
              X
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tabletView: Boolean
  },
  data() {
    return {
      clicked: false
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header-container {
}
.header-container-tablet {
}
#header {
  background: $black;
  color: $light-grey;
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
    .arrow-drop {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 25%;
    }
  }
  .burger-content {
    ul {
      display: flex;
      flex-direction: column;
      box-shadow: -9px 0px 18px 0px #00000029;
    }
    a {
      font-weight: 600;
      color: $light-grey;
    }
  }
  ul {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  a {
    font-weight: 600;
    color: $light-grey;
    padding-right: 20px;
  }
}

/**:first-child */
i {
  font-size: 2rem;
}
.tablet-nav-links {
  position: fixed;
  top: 0;
  right: 0;
  list-style: none;
  display: flex;
  flex-direction: column;
  padding: 30px 1rem 0 1rem;
  background: white;
  height: 100%;
  z-index: 2;
  width: 50%;
  background: $black;
  li {
    display: flex;
    justify-content: flex-end;
    padding: 1rem;
    a {
      transition: all 0.3s ease 0s;
    }
  }
}
.nav-links li {
  display: inline-block;
  padding: 0px 20px;
}
.nav-links li a {
  transition: all 0.3s ease 0s;
}
.nav-links li a:hover {
  color: #7f54b3;
}
.close {
  position: fixed;
  top: 1rem;
  right: 2rem;
  color: #fff;
  z-index: 3;
}
</style>
