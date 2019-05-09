<template lang="pug">
  div#main-achievements
    div
      h1(v-show='!isJpn') Achievements
      h1(v-show='isJpn') 実績
      div.list
        web.content(:isJpn='isJpn')
        mobile.content(:isJpn='isJpn')
</template>


<script>
import Mobile from './achievements/Mobile'
import Web from './achievements/Web'

export default {
  name: 'achievements',
  props: [ 'isJpn' ],
  components: {
    Mobile,
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
      }
    }
  }
</style>
