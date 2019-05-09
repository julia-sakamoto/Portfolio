<template lang="pug">
  div#main-about
    h1(v-show='!isJpn') About
    h1(v-show='isJpn') プロフィール
    div.about-content
      p(v-show='!isJpn') {{ eng }}
      p(v-show='isJpn') {{ jpn }}
      div.img
</template>


<script>
export default {
  name: 'about',
  props: ['isJpn'],
  data() {
    return {
      eng: `A freelance developer and current Sheridan College student. Set to graduate in December of 2019, I am a multi-disciplined developer who's strength lies within the following languages:
      Javascript (Vue.js, React + React Native, Angular, etc) C# with .NET, and Java. As a fluent Japanese speaker, I may also assist in translations for websites and other documents. Available for freelance hiring.`,
      jpn: `フリーランスであり、学生でもあるウェブエンジニアです。仕事の経験は一年ほどあり、プロとして仕事を対応いたします。使いこなせる言語は、Javascript (Vue.js, React + React Native, Angular, etc)、.Net (C#)、そしてJavaがあります。
      柔軟に対応が可能な上、英語と日本語を使った多言語対応もできます。まずはお気軽にお問い合わせください。`
    }
  }
}
</script>

<style lang="less">
#main-about {
  z-index: 100;
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
      background-position-y: 50%;
      background-repeat: no-repeat;
      width: 80%;
    }
  }
}
</style>
