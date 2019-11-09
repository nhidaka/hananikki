<template>
  <div class="top">
    <div class="header">
      <p><img src="../assets/hananikki/logo_black.png" alt=""></p>
      <div class="sns">
        <a href="https://www.mercari.com/jp/u/112250549/" target="_blank"><img src="../assets/hananikki/mercari_icon.png" class="mercari"></a>
        <a href="https://minne.com/@oyukinko" target="_blank"><img src="../assets/hananikki/minne_appicon.png"></a>
        <a href="https://fril.jp/shop/f3a200e87b5d9594910a941f7568ce1d" target="_blank"><img src="../assets/hananikki/Rakuma-appicon.png"></a>
      </div>
    </div>
    <div class="contents">
      <p>ドライフラワー・花材販売</p>
      <p class="title">FLOWER ARRANGE</p>
    </div>
    <Intro/>
    <Items/>
    <News/>
    <Map/>
    <Footer/>
  </div>
</template>

<script>
import Intro from "./Intro"
import Items from "./Items"
import News from "./News"
import Map from "./Map"
import Footer from "./Footer"

export default {
  name: 'Top',
  components: {
    Intro,
    Items,
    News,
    Map,
    Footer
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.top {
  height: 100vh;
  background-image: url(./../assets/hananikki/back_2.jpg);
  background-repeat:no-repeat;
  background-size: cover;
}

.top .header {
  padding: 32px 32px 0 32px;
  display: flex;
  justify-content: space-between;
}

.top .header p img {
  width: 160px;
  height: auto;
}

.top .header img {
  width: 24px;
  height: 24px;
  margin-bottom: 8px;
  margin-right: 6px;
}

.top .header img.mercari {
  width: 36px;
  height: 36px;
  margin: 0;
}

.top .header p {
  margin: 0;
  text-align: left;
  font-size: 20px;
}

.top .contents {
  height: calc(100% - 59px);
  position: relative;
}

.top .contents p {
  color: #fff;
  margin: 0 auto;
  padding: 16px;
  display: inline-block;
  position: absolute;
  bottom: 56%;
  left: 41%;
}

.top .contents p.title {
  background-color: rgba(255,255,255,0.5);
  border: 1px solid rgba(119, 119, 119, 0.5);
  color: #777;
  font-size: 32px;
  bottom: 46%;
  left: 36%;
}

@media screen and (max-width:769px) {
  .top .contents p.title {
    bottom: 51%;
    left: 27%;
  }

  .top .contents p {
    bottom: 62%;
    left: 35%;
    color: #555;
  }
}

@media screen and (max-width:479px) {
  .top {
    background-position: center;
  }

  .top .contents p {
    left: 32%;
    bottom: 61%;
    font-size: 12px;
  }

  .top .contents p.title {
    font-size: 24px;
    left: 20%;
  }
}

@media screen and (max-width:376px) {
  .top {
    background-position: center;
  }

  .top .contents p {
    bottom: 59%;
    left: 28%;
    padding: 12px;
  }

  .top .contents p.title {
    left: 16%;
    padding: 9px;
  }
}


</style>
