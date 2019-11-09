<template>
  <div class="map">
    <h2>ACCESS</h2>
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3288.2879323476723!2d133.3895523152207!3d34.4955839804877!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x35511148d62a9359%3A0x1db28a428682fd36!2z44OV44Op44Ov44O844K344On44OD44OX44Oe44OE44Km44Op!5e0!3m2!1sja!2sjp!4v1573228866044!5m2!1sja!2sjp" width="1200" height="400" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
  </div>
</template>

<script>
export default {
  name: 'Map'
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

h2 {
  text-align: center;
  margin-bottom: 32px;
}

.map {
  color: #555;
  text-align: left;
  padding-top: 8%;
}

.map iframe {
  width: 100%;
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  -ms-filter: grayscale(100%);
  -o-filter: grayscale(100%);
  filter: grayscale(100%);
}

iframe:hover {
  transition: filter 0.8s ease;
  -webkit-filter: grayscale(0%);
  -moz-filter: grayscale(0%);
  -ms-filter: grayscale(0%);
  -o-filter: grayscale(0%);
  filter: grayscale(0%);
}

</style>
