<template lang="pug">
  div#home
    div.title-text
      h1 Julia Sakamoto
      h3 Web Portfolio
      div.sns
        a(v-for='link in sns' :href='link.url')
          img.imgs(:src='link.img')
</template>


<script>
export default {
  name: 'home',
  data() {
    return {
      sns: [
        { url: 'https://twitter.com/ShiusMusic', img: require('../assets/sns/twitter.png') },
        { url: 'https://www.youtube.com/channel/UCF_tfmZcciaGyoDO14q_LvA', img: require('../assets/sns/youtube.png') },
        { url: 'https://open.spotify.com/artist/5rtPxYOqAocKkPSv8A808c', img: require('../assets/sns/spotify.png') },
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
      width: 30px;
      height: auto;
      filter: invert(100%);
    }
  }
  .title-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    line-height: 0%;
  }
</style>
