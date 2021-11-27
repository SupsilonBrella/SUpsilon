<!doctype html>
<html>
<head>
<meta charset="utf-8">
 
</head>
 
<body>
<div style="text-align: center;">
<div style="background: url(http://www.scr-wiki.top/local--files/component:theme/notion.png) center no-repeat; float: center; border: solid 2px #000; padding: 1px 15px; box-shadow: 0 1px 3px rgba(0,0,0,.2);">
<br />
<span style="font-size:larger;"><span style="color:red">距离该倒计时结束还有：</span>
<hr />
<br />
<div id="CountMsg" class="HotDate">
<span style="font-size:larger;"><span style="color: red"><span id="t_d">00天</span></span></span>
<span style="font-size:larger;"><span style="color: red"><span id="t_h">00时</span></span></span>
<span style="font-size:larger;"><span style="color: red"><span id="t_m">00分</span></span></span>
<span style="font-size:larger;"><span style="color: red"><span id="t_s">00秒</span></span></span>
</div>
<br />
<br />
</div>
</div>

<script type="text/javascript">
function getRTime(){
var EndTime= new Date('{$year}/{$month}/{$day}'); //截止时间
var NowTime = new Date();
var t =EndTime.getTime() - NowTime.getTime();
/*var d=Math.floor(t/1000/60/60/24);
t-=d*(1000*60*60*24);
var h=Math.floor(t/1000/60/60);
t-=h*60*60*1000;
var m=Math.floor(t/1000/60);
t-=m*60*1000;
var s=Math.floor(t/1000);*/
 
var d=Math.floor(t/1000/60/60/24);
var h=Math.floor(t/1000/60/60%24);
var m=Math.floor(t/1000/60%60);
var s=Math.floor(t/1000%60);
 
document.getElementById("t_d").innerHTML = d + "天";
document.getElementById("t_h").innerHTML = h + "时";
document.getElementById("t_m").innerHTML = m + "分";
document.getElementById("t_s").innerHTML = s + "秒";
}
setInterval(getRTime,1000);
</script>
</body>
</html>
