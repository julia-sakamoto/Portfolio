<template lang="pug">
    div#to-top(@click='toTop()' v-show='!isTop')
      div
</template>


<script>
export default {
  name: 'top',
  data() {
    return {
      isTop: true
    }
  },
  methods: {
    toTop() {
      window.scroll({
      top: 0,
      left: 0,
      behavior: 'smooth'
      });
    },
    handleScroll() {
      this.isTop = window.scrollY > 100 ? false : true;
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll);
  }
}
</script>

<style lang="less">
  #to-top {
    cursor: pointer;
    position: fixed;
    bottom: 2%;
    right: 1%;
    width: calc(25px + 1vw);
    height: calc(25px + 1vw);
    display: flex;
    justify-content: center;
    align-items: center;
    div {
      width: calc(25px + 1vw);
      height: calc(25px + 1vw);
      border-radius: 5px;
      background-color: antiquewhite;
      overflow: hidden;
      -webkit-clip-path: polygon(25% 0, 100% 50%, 25% 100%, 0% 100%, 75% 50%, 0 0);
      clip-path: polygon(25% 0, 100% 50%, 25% 100%, 0% 100%, 75% 50%, 0 0);
      transform: rotate(-90deg);
    }
  }
</style>
