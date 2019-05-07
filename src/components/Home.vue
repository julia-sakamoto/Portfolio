<template lang="pug">
  div#main-home
    div.title-text
      h1 Julia Sakamoto
      h3 Interactive Portfolio
</template>


<script>
export default {
  name: 'home'
}
</script>

<style lang="less">
  #main-home {
    background-image: url('../assets/moon.png');
    background-color: #1b2842;
    background-blend-mode: color-dodge;
    background-size: 100%;
    background-position-y: 50%;
    .title-text {
      mix-blend-mode: difference;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }
</style>
