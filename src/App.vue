<template lang="pug">
  div
    home
    about
    achievements
    contact
    menu
    top
</template>


<script>
import Home from './components/Home'
import About from './components/About'
import Achievements from './components/Achievements'
import Contact from './components/Contact'
import Menu from './components/overlay/Menu'
import Top from './components/overlay/Top'

export default {
  name: 'app',
  components: {
    Home,
    About,
    Achievements,
    Contact,
    Menu,
    Top
  }
}
</script>

<style lang="less">

</style>

