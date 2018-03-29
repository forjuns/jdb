<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>2017监督部</title>
<style type="text/css">
body{
background:#000000;
margin:20px 0;
font:12px Verdana,Arial,Tahoma;text-align:center;vertical-align:middle;color:#FFFFFF
}	
img{
border:none
}
.txt_1{
font:bold 24px Verdana,Tahoma;
color:#fff
}
img.thumb_img{
cursor:pointer;
display:block;
margin-bottom:10px
}
img#main_img{
cursor:pointer;
display:block;
}
#gotop{
cursor:pointer;
display:block;
}
#gobottom{
cursor:pointer;
display:block;
}
#showArea{
height:"355px";
margin:"10px";
overflow:hidden
}
</style>
<!--<script src="js/jquery3.1.1.js"></script>-->

</head>
<body>
<table width="760" border="0" align="center" cellpadding="0" cellspacing="8">
<tr>
<td height="75" colspan="2" align="left" class="txt_1">2017监督部</td>
</tr>
<tr>
<td width="640" align="center">
<!--	<button id="main_img">点击<双击查看原图tton>-->
<img src="img/01.jpg" width="900" height="800" border="0" id="main_img" >
</td>
<td width="110" align="center" valign="top">
<img src="img/01.jpg" width="100" height="10" id="gotop" altat="#"  />
<div id="showArea">
<img src="img/01.jpg" alta="#" width="80" height="50" border="0" class="thumb_img" />
<img src="img/02.jpg" alta="#" width="80" height="50" border="0" class="thumb_img"  />
<img src="img/03.jpg" alta="#" width="80" height="50" border="0" class="thumb_img"  />
<img src="img/04.jpg" alta="#" width="80" height="50" border="0" class="thumb_img" />
<img src="img/05.jpg" alta="#" width="80" height="50" border="0" class="thumb_img" />
<img src="img/06.jpg" alta="#" width="80" height="50" border="0" class="thumb_img" />
<img src="img/07.jpg" alta="#" width="80" height="50" border="0" class="thumb_img" />
<img src="img/08.jpg" alta="#" width="80" height="50" border="0" class="thumb_img"  />
<img src="img/09.jpg" alta="#" width="80" height="50" border="0" class="thumb_img"  />
</div>
<img src="img/09.jpg" width="100" height="14" id="gobottom" />
</td>
</tr>
</table>
<br />
<p>&nbsp</p>
<script type="application/javascript">
function $(e){
return document.getElementById(e);
}
document.getElementsByClassName=function(cl){
var retnode=[];
var myclass=new RegExp('\\b'+ cl+'\\b');
var elem=this.getElementsByTagName('*');
for(var i=0;i<elem.length;i++){
var classes=elem[i].className;
if(myclass.test(classes))
 retnode.push(elem[i]);
}
return retnode;
}
var MyMar;
var speed=1;
var spec=1;
var ipath='img/';

var thumbs=document.getElementsByClassName('thumb_img');
for(var i=0;i<thumbs.length;i++){
thumbs[i].onmouseover=function(){
/*$('main_img').src=this.rel;*/
$('main_img').src=this.src;
}
thumbs[i].onclick=function(){
location=this.src
}
}
document.getElementById('main_img').onclick=function(){
location=this.src;
}
$('gotop').onmouseover=function(){
this.src=ipath+'01.jpg';
MyMar=setInterval(gotop.speed);
}
$('gotop').onmouseout=function(){
this.src=ipath+'01.jpg';
clearInterval(MyMar);
}
$('gobottom').onmouseover=function(){
this.src=ipath+'09.jpg';
MyMar=setInterval(gobottom.speed);
}
$('gobottom').onmouseout=function(){
this.src=ipath+'09.jpg';
clearInterval(MyMar);
}
function gotop(){
document.getElementById('showArea').scrollTop-=spec;
}
function gobottom(){
document.getElementById('showArea').scrollTop+=spec;
}
</script>
</body>
</html>
