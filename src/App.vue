<template lang="pug">
  div
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

</style>

