<template lang="pug">
  div#main-achievements
    h1 Achievements
    div.list
      mobile
      music
      web
</template>


<script>
import Mobile from './achievements/Mobile'
import Music from './achievements/Music'
import Web from './achievements/Web'

export default {
  name: 'achievements',
  components: {
    Mobile,
    Music,
    Web
  }
}
</script>

<style lang="less">
  #main-achievements {
    background-color: #1b2842;
    .list {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
    }
  }
</style>
