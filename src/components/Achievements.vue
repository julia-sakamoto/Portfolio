<template lang="pug">
  div#main-achievements
    h1 Achievements
    div.list
      mobile.content
      web.content
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
    background-color: #3b5a8d;
    padding: 5%;
    .list {
      .content {
        width: 100%;
        size: 0em;
      }
    }
  }
</style>
