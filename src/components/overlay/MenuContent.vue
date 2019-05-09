<template lang="pug">
  transition(name='slide-in')
    div#menu
      p(v-show="!isJpn" @click='$emit("toggleLang")') 日本語
      p(v-show="isJpn" @click='$emit("toggleLang")') English
      p(v-show='!isJpn' @click='$emit("toBottom")') Contact
      p(v-show='isJpn' @click='$emit("toBottom")') お問合せ 
</template>

<script>
export default {
  name: 'menu-content',
  props: [ 'isJpn' ]
}
</script>

<style lang="less">
  .slide-in-enter-active, .slide-in-leave-active {
    transition: all .5s ease;
  }
  .slide-in-enter, .slide-in-leave-to {
    transform: translateY(10px);
    opacity: 0;
  }
  #menu {
    z-index: 100;
    position: fixed;
    top: 10%;
    background-color: antiquewhite;
    width: 50%;
    color: #2c2d2d;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: baseline;
    transition: all .3s ease;
    p {
      cursor: pointer;
    }
  }
</style>
