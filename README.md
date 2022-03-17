# BanJS

### 前端引用

#### 1.body加入 <body 加入到这儿>
```css
onselectstart="return false" //禁止右键复制
 ```

#### 2.引入

```css
<script>
function click(e) {
if (document.all) {
if (event.button==2||event.button==3) { alert("禁止访问");
oncontextmenu='return false';
}
}
if (document.layers) {
if (e.which == 3) {
oncontextmenu='return false';
}
}
}
if (document.layers) {
document.captureEvents(Event.MOUSEDOWN);
}
document.onmousedown=click;
document.oncontextmenu = new Function("return false;")
document.onkeydown =document.onkeyup = document.onkeypress=function(){ 
if(window.event.keyCode == 123) { 
window.event.returnValue=false;
return(false); 
} 
}
</script>


<!--禁用审查元素-->

<script src="http://namexample.com/banJS/console-ban.min.js"></script>
<script>
// default options
ConsoleBan.init()
// custom options
ConsoleBan.init({
redirect: '/404.html'
})
</script>
```
