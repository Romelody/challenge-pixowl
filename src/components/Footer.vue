<template>
  <div id="footer">
    <div class="container content padding-y">
      <div class="footer-logo">
        <img src="../assets/img/tsblogo.svg" alt="" />
      </div>
      <div class="pages">
        <p class="footer-title">Pages</p>
        <div class="lists">
          <div class="list-pages">
            <a href="#">Start</a>
            <a href="#">Shop</a>
            <a href="#">Create</a>
            <a href="#">Play</a>
          </div>
          <div class="list-pages">
            <a href="#">Me</a>
            <a href="#">Map</a>
            <a href="#">SAND</a>
            <a href="#">Account</a>
          </div>
        </div>
      </div>
      <div class="social-media">
        <p class="footer-title">Social</p>
        <div class="social-icon">
          <a href="https://discord.com/invite/X3Gw8NC"
            ><img src="../assets/img/discord-logo.svg" alt="Discord"
          /></a>
          <a href="https://t.me/sandboxgame">
            <img src="../assets/img/telegram-logo.svg" alt="Telegram"
          /></a>
          <a href="https://medium.com/sandbox-game">
            <img src="../assets/img/medium-logo.svg" alt="Medium"
          /></a>
        </div>
        <div class="social-icon">
          <a href="https://twitter.com/thesandboxgame"
            ><img src="../assets/img/twitter-logo.svg" alt="Twitter"
          /></a>
          <a href="https://www.instagram.com/thesandboxgame/"
            ><img src="../assets/img/instagram-logo.svg" alt="Instagram"
          /></a>
          <a href="https://www.facebook.com/TheSandboxGame/"
            ><img src="../assets/img/facebook-logo.svg" alt="Facebook"
          /></a>
        </div>
      </div>
    </div>
    <div class="copyright">
      <p>Copyright</p>
    </div>
  </div>
</template>
<style lang="scss" scoped>
#footer {
  background: $dark-grey;
  .content {
    display: flex;
    flex-direction: row;
  }
  .footer-logo {
    width: 33%;
    display: flex;
    justify-content: center;
  }
  .pages {
    width: 33%;
    .lists {
      display: flex;
      flex-direction: row;
    }
  }
  .social-media {
    width: 33%;
  }
  .footer-title {
    color: $white;
    font-size: 25px;
    text-transform: uppercase;
    font-weight: 800;
    padding-bottom: 24px;
  }
  .list-pages {
    margin-right: 110px;
    display: flex;
    flex-direction: column;
    font-size: 20px;
    a {
      margin-bottom: 15px;
      color: $light-grey;
      &:hover {
        color: $white;
        font-weight: 600;
      }
    }
  }
  .social-icon {
    padding-bottom: 20px;
    :first-child {
      padding-left: 0px;
    }
    :last-child {
      padding-right: 0px;
    }
    img {
      &:hover {
        @keyframes spin {
          from {
            transform: rotate(0deg);
          }
          to {
            transform: rotate(360deg);
          }
        }
        animation: spin 2s;
      }
    }
    a {
      cursor: pointer;
      width: 60px;
      height: 60px;
      padding: 10px;
    }
  }
}
.copyright {
  background: $black;
  text-align: center;
  padding: 20px;
  color: $medium-grey;
}
</style>
