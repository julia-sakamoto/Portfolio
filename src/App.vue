<template lang="pug">
  div.main
    home
    about
    achievements
    contact
    site-menu
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
  }
}
</script>

<style lang="less">
body {
  background-color: #121213;
  height: 100%;
  color: antiquewhite;
  font-family: 'Abel';
  margin: 0%;
  .main {
    display: flex;
    flex-direction: column;
      font-size: 2.5em;
  }
}
</style>

