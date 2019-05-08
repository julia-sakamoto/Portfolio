<template lang="pug">
  div#menu
    div.menu-icon
      div.bar
      div.bar
      div.bar
    div.menu-exit
</template>


<script>
export default {
  name: 'site-menu'
}
</script>

<style lang="less">
  #menu {
    position: fixed;
    top: 3%;
    left: 1%;
    .menu-icon {
      width: 30px;
      height: 30px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      .bar {
        width: 30px;
        height: 2px;
        background-color: antiquewhite;

      }
    }
  }
</style>
