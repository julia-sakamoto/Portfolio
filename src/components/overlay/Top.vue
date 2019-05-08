<template lang="pug">
  div#to-top
    div#triangle-up
</template>


<script>
export default {
  name: 'top'
}
</script>

<style lang="less">
  #to-top {
    position: fixed;
    bottom: 2%;
    right: 1%;
    background-color: antiquewhite;
    width: 45px;
    height: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    #triangle-up {
      width: 0;
      height: 0;
      border-left: 15px solid transparent;
      border-right: 15px solid transparent;
      border-bottom: 30px solid #261758;
    }
  
  }
</style>
