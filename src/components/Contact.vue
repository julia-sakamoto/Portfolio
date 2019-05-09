<template lang="pug">
  div#main-contact
    div(v-show='!isJpn')
      p Contact:
      p nateisshius@gmail.com
    div(v-show='isJpn')
      p お問合せ
      p nateisshius@gmail.com
</template>


<script>
export default {
  name: 'contact',
  props: [ 'isJpn' ]
}
</script>

<style lang="less">
#main-contact {
  div {
    display: flex;
    justify-content: space-evenly;
  }
}
</style>
