### Javasript

```javascript
//输出
document.write("<h1>This is a heading</h1>");           //写入html输出
document.getElementById("demo").innerHTML="Hello JavaScript";          //查找html元素并改变其内容
document.getElementById("demo").style.color="#ff0000";        //查找html元素并改变其样式

//语句
var name="Hello"; var name = "Hello";     //JS忽略脚本中的空格，“;”用来分隔语句和在同一行写多条语句，“;”是可选的
document.write("hello \                        
world");                                         //在文本字符串中使用\来实现换行
//变量
var x=2, y=x+1, z="string";               //声明变量并赋值,","用以分隔变量，也可以多行书写
var x;                                   //未赋值的变量值统一为undefined
var x=2; var x;                         //重新声明后x的值仍为2
//数据类型：字符串string、数字number、布尔boolean、数组array、对象object、Null、Undefined
var a=true， b=false;           //布尔逻辑值
var cars=new Array();           //通过new声明变量类型为数组
cars[0]="Audi";
cars[1]="BMW";
cars[2]="Volvo";
var cars=new Array("Audi","BMW","Volvo");    
var cars=["Audi","BMW","Volvo"];                           
var person={firstname:"Bill", lastname:"Gates", id:5566};   //对象属性以name:value来定义，对象有属性和方法
objectName.popertyName         //访问对象属性
objectName.methodName          //访问对象方法
```

### jQuery

```js
// 安装
<head>
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.0/jquery.min.js">
</script>
</head>

// 语法
$(document).ready(function(){
  $("selector").action()
});

$("button").click(function(){
  $("p").hide()
});

// 效果
$('p').hide(speed,callback);   // hide/show/toggle   隐藏/显示  
$('p').fadeIn(speed,callback); // fadeIn/fadeOut/fadeToggle/fadeTo  淡入/淡出
$('p').slideDown(speed,callback);  // slideDown/slideUp/slideToggle  滑动
$('p').animate({params},speed,callback);  // {params}为css，但使用camel语法，且属性值可设为'show/hide/toggle'  动画
$('p').stop(stopAll,stopToEnd);  // 停止效果，默认参数值都为false
$("#p1").css("color","red").slideUp(2000).slideDown(2000);  // 链接

// html
$().text(function(i,origText){                           // text(),html(),val() 文本值/html值/表单值
  return i +'为下标，' + origText +'为原始值'
});  
$().attr(function(i,origText));  // 属性的值
$().append() // append/prepend/before/after
$().remove()  // remove/empty
$().addClass() // addClass/removeClass/toggleClass  css类
$().css("background-color","red");
$().width()  //width/height/innerWidth/outerWidth

// 遍历
$().parent()  //parent/parents/parentsUntill
$().children()  //children/find
$().siblings()  //siblings/next/nextAll/nextUntill/prev/prevAll/prevUntill
$().first()  //first/last/eq/filter/not
```

### Ajax

```js
$().load(URL,data,callback);  // callback  function(responseText,statusText,xhr)
$.get(URL,callback)
$.post(URL,data,callback)
$.ajax({url:"test.js",dataType:"json",type:"get",success:callback});

function sample()
{
var xmlhttp=new XMLHttpRequest();
xmlhttp.onreadystatechange=function()
  { if (xmlhttp.readyStage==4 && xmlhttp.status==200)
      {document.getElementById("id1").innerHTML=xmlhttp.responseText;}
  }
xmlhttp.open("GET",URL,true);
xmlttp.send();
}
```



