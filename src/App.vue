<template lang="pug">
  div.main
    div.sun
    div.moon
      div.inner
    div.stars
      p
    div.home
      home
    div.content
      achievements
      about
      contact
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
import SiteMenu from './components/overlay/SiteMenu'
import Top from './components/overlay/Top'

export default {
  name: 'app',
  components: {
    Home,
    About,
    Achievements,
    Contact,
    SiteMenu,
    Top
  },
  data() {
    return {
      isJpn: false,
      isMenu: false,
    }
  },
  methods: {
    changeEng() {
      this.isJpn = false;
    },
    changeJpn() {
      this.isJpn = true;
    },
    clickMenu() {
      this.isMenu = !this.isMenu;
    }
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
    font-size: 2.5em;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 5%;
    .sun {
      position: absolute;
    }
    .moon {
      position: absolute;
      right: 5%;
      top: 15%;
      display: block;
      box-shadow: inset 20px -30px 0 20px aliceblue;
      background-color: transparent;
      width: 350px;
      height: 350px;
      border-radius: 50%;        
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
      left: 1%;
      .menu-icon {
        width: 30px;
        height: 30px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        .bar {
          width: 30px;
          height: 2px;
          background-color: antiquewhite;
        }
      }
      .menu-exit {
        width: 30px;
        height: 30px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        .x-left {
          width: 35px;
          height: 4px;
          position: absolute;
          top: 25%;
          transform: rotate(45deg);
          background-color: antiquewhite;
        }
        .x-right {
          width: 35px;
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

