<template lang="pug">
  div
    div(v-show='!isJpn')
      h3 Mobile
      p {{ eng }}
    div(v-show='isJpn')
      h3  モバイル開発
      p {{ jpn }}
    div.links
      a(href='https://sirutasu.com/') SIRU+    
</template>


<script>
export default {
  name: 'mobile',
  props: ['isJpn'],
  data() {
    return {
      eng: 'As for mobile development, I have experienced developing a mobile application from start to finish. In my last internship at Bravesoft, I was part of an agile front-end development team, for a mobile application project known as "SIRU+". I was involved from beginning to end, and in charge of areas from front-end to testing. I have a sure grasp on the development lifecycle of mobile applications, and the experience to boot.',
      jpn: 'モバイル開発の実績は、ブレイブソフトのインターンで作った「SIRU+」があります。SIRU+の制作は、最初から最後までフロントエンドの開発チームの一部として関わっていました。アプリのコーディング、フロントエンドの開発、そしてテストを担当していました。アプリ開発のライフサイクルはしっかりと理解している上、更にプロとしての経験もあります。気軽にお問い合わせください。'
    }
  }
}
</script>

<style lang="less">

</style>
