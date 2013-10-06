---
title: test animator
date : 2012-11-30
--- &lead
  
<link  rel='stylesheet'
  href="../libraries/widgets/scianimator/css/scianimator.css">
<script src="../libraries/widgets/scianimator/assets/js/jquery-1.4.4.min.js"></script>
<script 
  src="../libraries/widgets/scianimator/assets/js/jquery.scianimator.pack.js">
</script>



```r
library(animation)
opts_chunk$set(fig.path = "assets/fig/testanimator-")
opts_knit$set(animation.fun = hook_scianimator)
```



```r
ani.options(nmax = 50)  # create 50 image frames
set.seed(20121106)
brownian.motion(n = 20, pch = 21, cex = 4, col = "red", bg = "yellow", xlim = c(-10, 
    10), ylim = c(-15, 15))
```


<div class="scianimator">
<div id="bw_fun" style="display: inline-block;">
</div>
</div>
<script type="text/javascript">
  (function($) {
    $(document).ready(function() {
      var imgs = Array(50);
      for (i=0; ; i++) {
        if (i == imgs.length) break;
        imgs[i] = "assets/fig/testanimator-bw-fun" + (i + 1) + ".png";
      }
      $("#bw_fun").scianimator({
          "images": imgs,
          "delay": 200,
          "controls": ["first", "previous", "play", "next", "last", "loop", "speed"],
      });
      $("#bw_fun").scianimator("play");
    });
  })(jQuery);
</script>


