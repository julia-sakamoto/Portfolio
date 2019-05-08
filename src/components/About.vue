<template lang="pug">
  div#main-about
    h1 About
    div.about-content
      p {{ etc }}
      div.img
</template>


<script>
export default {
  name: 'about',
  data() {
    return {
      etc: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed facilisis nibh urna. In feugiat, ex id lobortis finibus, augue velit scelerisque lectus, sit amet fermentum odio quam ac mauris.`
    }
  }
}
</script>

<style lang="less">
  .about-content {
    display: flex;
    justify-content: space-between;
    width: 100%;
    p {
      width: 100%;
    }
    .img {
      background-image: url('../assets/me.jpg');
      background-size: 60%;
      background-position-x: 100%;
      background-repeat: no-repeat;
      width: 80%;
    }
  }
</style>
