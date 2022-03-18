# BanJS

## An infrequent, somewhat useful project

### 前端引用

#### 1.body join <body ```java join here ```>
```css
onselectstart="return false" //禁止右键复制
 ```

#### 2.Introduce under the inedex file

```css
<!--禁用F12及鼠标键盘复制全选剪切功能-->
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
if(window.event.keyCode == Banjs) { 
window.event.returnValue=false;
return(false); 
} 
}
</script>


<!--禁用审查元素-->

<script src="https://raw.githubusercontent.com/0xDevops/BanJS/main/console-ban.min.js"></script> 
<script>
// default options
ConsoleBan.init()
// custom options
ConsoleBan.init({
redirect: '/404.html' //审查元素跳转404.html
})
</script>
```

#### Welcome Start
