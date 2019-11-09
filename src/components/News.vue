<template>
  <div class="news">
    <h2>NEWS</h2>
    <p>ニュースがまだ更新されていません。</p>
  </div>
</template>

<script>
export default {
  name: 'News'
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
  font-size: 12px;
}

.news {
  padding-top: 12%;
}



</style>
