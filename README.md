# jquery-easing-plugin
here it also use in scroll top, menu onclickc or anchor tag also use in toggle class and hide and show.  
 
plugin:- js

<!-- Plugin Jquery Easing -->
<script src="assets/js/jquery.easing.js"></script>

<!-- custom js plugin --> 
<script>
  ! function(a) {
    "use strict";
    a('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function() {
        if (location.pathname.replace(/^\//, "") == this.pathname.replace(/^\//, "") && location.hostname == this.hostname) {                     var o = a(this.hash);
        if ((o = o.length ? o : a("[name=" + this.hash.slice(1) + "]")).length) return a("html, body").animate({
          scrollTop: o.offset().top - 54
        }, 1e3, "easeInOutExpo"), !1
      }
    });
    a('.js-scroll-trigger-nav-2').click(function() {
      if (location.pathname.replace(/^\//, "") == this.pathname.replace(/^\//, "") && location.hostname == this.hostname) {
        var o = a(this.hash);
        if ((o = o.length ? o : a("[name=" + this.hash.slice(1) + "]")).length) return a("html, body").animate({ 
          scrollTop: o.offset().top - 54
        }, 1e3, "easeInOutQuart"), !1
      }       
    });
  }(jQuery);  
  
  In HTML :-
  <!-- add class in anchor tag -->
  <li class="nav-item active">
     <a class="nav-link js-scroll-trigger-nav-2" href="#service">services</a>
  </li>                     
  <li class="nav-item">  
    <a class="nav-link js-scroll-trigger-nav-2" href="#portfolio">portfolio</a>                   
  </li>   
  <li class="nav-item"> 
    <a class="nav-link js-scroll-trigger-nav-2" href="#about">about</a>  
  </li>
  <li class="nav-item"> 
    <a class="nav-link js-scroll-trigger-nav-2" href="#team">team</a> 
  </li>     
  <li class="nav-item">   
    <a class="nav-link js-scroll-trigger-nav-2" href="#contact">contact</a>
  </li> 
  <!-- add class in button -->  
  <!-- which is first js custom plugin -->
  <a class="header-btn btn btn-lg text-capitalize btn-primary js-scroll-trigger" href="#service">Tell Me More</a>
