<template lang="pug">
  div.main
    menu-content(v-show='isMenu' @click='clickMenu()' :isJpn='isJpn' @toggleLang='toggleLang()' @toBottom='toBottom()')
    div.moon
      div.inner
    div.stars
    div.home
      home(:isJpn='isJpn')
    div.content
      achievements(:isJpn='isJpn')
      about(:isJpn='isJpn')
      contact(:isJpn='isJpn')
    div.menu
      div.menu-icon(v-show='!isMenu' @click='clickMenu()')
        div.bar
        div.bar
        div.bar
      div.menu-exit(v-show='isMenu' @click='clickMenu()')
        div.x-left
        div.x-right
    top
</template>


<script>
import Home from './components/Home'
import About from './components/About'
import Achievements from './components/Achievements'
import Contact from './components/Contact'
import Top from './components/overlay/Top'
import MenuContent from './components/overlay/MenuContent'

export default {
  name: 'app',
  components: {
    Home,
    About,
    Achievements,
    Contact,
    Top,
    MenuContent
  },
  data() {
    return {
      isJpn: true,
      isMenu: false,
    }
  },
  methods: {
    toggleLang() {
      this.isJpn = !this.isJpn;
    },
    clickMenu() {
      this.isMenu = !this.isMenu;
    },
    toBottom() {
      window.scroll({
        top: document.body.scrollHeight,
        left: 0,
        behavior: 'smooth'
      });
    }
  },
  beforeMount() {
    window.scrollTo(0, 0);
  }
}
</script>

<style lang="less">
body {
  height: 100%;
  color: antiquewhite;
  font-family: 'Abel';
  margin: 0%;
  .main {
    background: #1e5799; /* Old browsers */
    background: -moz-linear-gradient(top, #1e5799 0%, #ff6f3f 96%, #ff6f3f 100%); /* FF3.6-15 */
    background: -webkit-linear-gradient(top, #1e5799 0%,#ff6f3f 96%,#ff6f3f 100%); /* Chrome10-25,Safari5.1-6 */
    background: linear-gradient(to bottom, #1e5799 0%,#ff6f3f 96%,#ff6f3f 100%);
    font-size: calc(0.5em + 2.3vw);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 5%;
    min-height: 100%;
    .moon {
      position: absolute;
      right: 5vw;
      top: 15vw;
      display: block;
      box-shadow: inset 20px -30px 0 20px aliceblue;
      background-color: transparent;
      width: calc(100px + 20vw);
      height: calc(100px + 20vw);
      border-radius: 50%;
      mix-blend-mode: overlay;        
    }
    .stars {
      width: 100%;
      height: 150%;
      mix-blend-mode: lighten;
      position: absolute;
      top: 0%;
      background-image: url('./assets/stars.png');
      background-size: 45%;
      background-repeat: repeat-x;
    }
    .home {
      position: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .content {
      width: 90%;
    }
    .menu{
      position: fixed;
      top: 3%;
      left: 1.5vw;
      width: calc(20px + 1vw);
      height: calc(20px + 1vw);
      cursor: pointer;
      .menu-icon {
        width: calc(20px + 1vw);
        height: calc(15px + 1vw);
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        .bar {
          width: calc(20px + 1vw);
          height: 2px;
          background-color: antiquewhite;
        }
      }
      .menu-exit {
        width: calc(20px + 1vw);
        height: calc(20px + 1vw);
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        .x-left {
          width: calc(20px + 1vw);
          height: 4px;
          position: absolute;
          top: 25%;
          transform: rotate(45deg);
          background-color: antiquewhite;
        }
        .x-right {
          width: calc(20px + 1vw);
          height: 4px;
          position: absolute;
          top: 25%;
          transform: rotate(-45deg);
          background-color: antiquewhite;
        }
      }
    }
  }
}
</style>

