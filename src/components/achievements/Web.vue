<template lang="pug">
  div#web
    div(v-show='!isJpn')
      h3 Web
      p {{ eng }}
    div(v-show='isJpn')
      h3  サイト制作
      p {{ jpn }}
    div.links
      a(href='https://www.tbs.co.jp/muryou-douga/') TBS FREE
      a(href='https://www.bravesoft.co.jp/blog/') brave one
</template>


<script>
export default {
  name: 'web',
  props: ['isJpn'],
  data() {
    return {
      eng: `With over a year of professional experience, my main achievements include working with Bravesoft to develop a website for Tokyo Broadcasting System Television's free streaming website, known as "TBS FREE". I've also worked on other webistes, such as Bravesoft's own technology blog, "brave one". Links to both websites can be found below.`,
      jpn: 'サイト制作は1年程の経験があり、主な仕事はブレイブソフトのインターンとして働いていた時にやりました。実績の中にはTBSFreeのウェブサイト制作や、ブレイブソフトの「brave one」ブログの改造があります。TBSFreeはホームページまで作成し、ブログはテーマの部分までコーディングしました。それぞれのサイトのリンクは以下になります。'
    }
  }
}
</script>

<style lang="less">
.links {
  display: flex;
  justify-content: space-evenly;
  a {
    color: aquamarine;
    align-self: center;
  }
}
</style>
