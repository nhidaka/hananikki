<template>
  <div class="footer">
    <div class="footer_blocks">
      <div class="logo"><img src="../assets/hananikki/logo.png" alt=""></div>
      <div class="sns">
        <a href="https://www.mercari.com/jp/u/112250549/" target="_blank"><img src="../assets/hananikki/mercari_icon.png" class="mercari"></a>
        <a href="https://minne.com/@oyukinko" target="_blank"><img src="../assets/hananikki/minne_appicon.png"></a>
        <a href="https://fril.jp/shop/f3a200e87b5d9594910a941f7568ce1d" target="_blank"><img src="../assets/hananikki/Rakuma-appicon.png"></a>
      </div>
    </div>
    <p>©︎2019 HANANIKKI inc.</p>
  </div>
</template>

<script>
export default {
  name: 'Footer'
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
  color: #fff;
  cursor: pointer;
}

p {
  color: #fff;
  font-size: 12px;
  position: absolute;
  left: 47%;
  bottom: 0;
  margin-bottom: 8px;
}

.footer {
  position: relative;
  color: #fff;
  text-align: left;
  background-color: #6d6966;
  height: 80px;
  padding: 3%
}

.footer .footer_blocks {
  display: flex;
  justify-content: space-between;
}

.footer .footer_blocks .logo img {
  width: 160px;
  height: auto;
}

.footer .footer_blocks img {
  width: 24px;
  height: 24px;
  margin-bottom: 8px;
  margin-right: 6px;
}

.footer .footer_blocks img.mercari {
  width: 36px;
  height: 36px;
  margin: 0;
}

@media screen and (max-width:769px) {
  p {
    text-align: center;
    position: static;
  }
}



</style>
