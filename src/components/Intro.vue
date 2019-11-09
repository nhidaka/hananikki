<template>
  <div class="intro">
    <div class="effect">
      <i class="fa fa-child fa-5x"></i>
      <div class="contents">
        <div class="explanation">
          <p class="sub_title">Introduction</p>
          <h2>HANANIKKI</h2>
          <p>花日記では、広島県福山市を中心にドライフラワーのアレンジ作品・花材の販売を行なっています。店舗での販売・配達・メルカリ等のアプリでも販売をしております。ぜひ一度作品をチェックしてみてください！</p>
        </div>
        <div class="image">
          <div class="image_bg"></div>
          <div></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Top'
}

$(function(){
  $('.effect div, .effect i').css("opacity","0");
  $(window).scroll(function (){
    $(".effect").each(function(){
      var imgPos = $(this).offset().top;
      var scroll = $(window).scrollTop();
      var windowHeight = $(window).height();
      if (scroll > imgPos - windowHeight + windowHeight/5){
        $("i, div",this).css("opacity","1" );
        $("i",this).css({
          "font-size": "100px",
          "padding": "0 20px 40px"
        });
      }
    });
  });
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.effect i {
  padding: 0 !important;
  transition: .2s;
}

.effect div {
  transition: .2s;
  transition-delay: .2s;
}

a {
  font-size: 12px;
  text-decoration: #555;
  color: #555;
  cursor: pointer;
}

p {
  line-height: 1.8;
}

.intro {
  color: #555;
  text-align: left;
}

.intro .contents {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding-top: 12%;
}

.intro .contents .explanation {
  width: calc(34% - 100px);
  display: inline-block;
  padding: 50px;
  padding-left: 140px;
}

.intro .contents .image {
  display: inline-block;
  height: 29vw;
  background-image: url(./../assets/hananikki/dryflower.jpg);
  background-repeat:no-repeat;
  background-size: cover;
  flex-basis: 56%;
  max-width: 56%;
}

@media screen and (max-width:769px) {
  .intro .contents {
    padding-top: 0;
  }

  .intro .contents .explanation {
    width: 100%;
    padding: 0 32px 32px;
  }

  .intro .contents .explanation h2{
    text-align: center;
    margin-top: 8px;
  }

  .intro .contents .explanation .sub_title {
    text-align: center;
    margin: 0;
  }



  .intro .contents .image {
    flex-basis: 100%;
    max-width: 100%;
    background-position: center;
  }
}

@media screen and (max-width:376px) {
.intro .contents .explanation {
    padding: 0 16px 16px;
  }
}


</style>
