<template lang="pug">
  div
    p Achievements
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

</style>
