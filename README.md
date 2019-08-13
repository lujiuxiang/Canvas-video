
# js
<pre>
<code>
var timer=null;
var video=document.getElementById('video1');
var canvas = document.getElementById("myCanvas");
var context = canvas.getContext("2d");
canvas.width = window.innerWidth*2;  //获取屏幕宽度作为canvas的宽度  这个设置的越大，画面越清晰（相当于绘制的图像大，然后被css缩小）
canvas.height = window.innerHeight*2;
function draw1() {
    video.play();
    timer = setInterval(function(){
      if(video.currentTime >=3.8){   //视频时间在3.8s时停止
         video.pause();
         clearInterval(timer);
      };
      context.drawImage(video, 0, 0, canvas.width, canvas.height);//绘制视频
   },16;
};
draw1()
</code>
</pre>
