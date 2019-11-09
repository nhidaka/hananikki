<template>
  <div class="items">
    <div class="effect">
      <i class="fa fa-child fa-5x"></i>
      <div class="contents">
        <div class="explanation">
          <h2>ITEMS</h2>
          <p>メルカリ・minne・ラクマなどでアレンジ作品を多数出品しております。</p>
        </div>
        <div class="image">
          <div class="b_img"><img src="../assets/hananikki/herbarium_2.png"></div>
          <div class="b_img"><img src="../assets/hananikki/herbarium_3.png"></div>
          <div class="b_img"><img src="../assets/hananikki/herbarium_4.png"></div>
          <div class="b_img"><img src="../assets/hananikki/flower.png"></div>
          <div class="b_img"><img src="../assets/hananikki/flower_2.png"></div>
          <div class="b_img"><img src="../assets/hananikki/flower_3.png"></div>
        </div>
        <div class="jump_sns">
          <a href="https://www.mercari.com/jp/u/112250549/" target="_blank">VIEW MORE</a>
          <p class="caution">※メルカリサイトに遷移します。</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Items'
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
  cursor: pointer;
}

.items {
  color: #555;
  text-align: left;
}

.items .contents {
  padding-top: 12%;
}

.items .contents .explanation {
  width: 100%;
  display: inline-block;
  text-align: center;
  order: 2;
}

.items .contents .jump_sns {
  margin: 12px auto 0;
  text-align: right;
  padding-right: 28px;
  max-width: 80%;
}

.items .contents .jump_sns a {
  display: block;
}

.items .contents .jump_sns a:hover {
  opacity: 0.8;
}

.items .contents .jump_sns .caution {
  font-size: 8px;
  margin: 4px 0 0;
}

.items .contents .image {
  order: 0;
  margin: 40px auto 0;
  max-width: 80%;
}

.items .contents .image .b_img {
  display: inline-block;
  width: 32%;
  margin-right: 0;
}

.items .contents .image .b_img img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

@media screen and (max-width:899px) {
  .intro .contents .explanation {
    padding-left: 100px;
  }
}

@media screen and (max-width:769px) {
  .items .contents {
    padding-top: 5%;
  }

  .items .contents .jump_sns {
    padding-right: 16px;
  }

  .items .contents .explanation p {
    margin: 0 16px;
  }
}

@media screen and (max-width:376px) {
  .items .contents .explanation p {
    margin: 16px;
    text-align: left;
  }

  .items .contents .image {
    max-width: 90%;
  }

  .items .contents .image .b_img {
    width: 32%;
  }

}

</style>
