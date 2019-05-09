<template lang="pug">
  div#home
    div.title-text
      div(v-show='!isJpn')
        h1 Julia Sakamoto
        h3 Web Portfolio
      div(v-show='isJpn')
        h1 坂本 樹理亜
        h3 ポートフォリオ
    div.sns
      a(v-for='link in sns' :href='link.url')
        img.imgs(:src='link.img')
</template>


<script>
export default {
  name: 'home',
  props: ['isJpn'],
  data() {
    return {
      sns: [
        // { url: 'https://twitter.com/ShiusMusic', img: require('../assets/sns/twitter.png') },
        // { url: 'https://www.youtube.com/channel/UCF_tfmZcciaGyoDO14q_LvA', img: require('../assets/sns/youtube.png') },
        // { url: 'https://open.spotify.com/artist/5rtPxYOqAocKkPSv8A808c', img: require('../assets/sns/spotify.png') },
        { url: 'https://github.com/julia-sakamoto', img: require('../assets/sns/github.png') },
        { url: 'https://www.linkedin.com/in/julia-batoon-sakamoto-76b4b0128/', img: require('../assets/sns/linkedin.png') }
      ]
    }
  }
}
</script>

<style lang="less">
  .sns {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    .imgs {
      width: calc(30px + 2vw);
      height: auto;
      filter: invert(100%);
    }
  }
  .title-text {
    div {
      display: flex;
      flex-direction: column;
      align-items: center;
      line-height: 0%;
    }
  }
</style>
