# javascript

## Javasript

```javascript
document.write("<h1>This is a heading</h1>");          
document.getElementById("demo").innerHTML="Hello JavaScript";         
document.getElementById("demo").style.color="#ff0000";       

//语句
var name="Hello"; var name = "Hello";     //JS忽略脚本中的空格，“;”用来分隔语句和在同一行写多条语句，“;”是可选的
document.write("hello \                        
world");                                         //在文本字符串中使用\来实现换行

//变量
var x=2, y=x+1, z="string";               //声明变量并赋值,","用以分隔变量，也可以多行书写
var x;                                   //未赋值的变量值统一为undefined
var x=2; var x;                         //重新声明后x的值仍为2

//字符串string、数字number、布尔boolean、数组array、对象object、Null、Undefined，其中array和 Null都是 object 类型
var cars=new Array();           //通过new声明的变量类型都是 object

// string method, tips: string can't be operated, so all operations will return a new string
str.split(',')    // split the string whit comma, returning an array
str.slice(start, end)    // extract string and return to a new string
str.substring(start, end)    // like str.slice(), but not support negative number of start and end
str.substr(start, length)
str.replace(old, new)    // replace the old string matching to a new string, supporting  regexp
str.toUpperCase()
str.concate(str1, str2)    // concate equals to plus +
str.trim()    // remove spaces at the beginning and end of the string
str.indexOf(str)

// number method
num.toString()

// array
array.length
array.sort()
array.reverse()
array.push()
array.pop()
array.shift()
array.unshift()
array.splice(insertStart, deleteNumber, insertElement)
array.toString()
array.join('delimiter')    // array.join(',') = array.toString
array.concate(array1, array2, ...)    // splice different arrays, return a new array
array.slice(start, end)    //return a new array
array.forEach(function)    // funtion(value, [index], [array])
array.map(funciton)    // funciton(value, [index], [array]), return a new array after executed for each element
array.filter(function)    // return a new array
```

## jQuery

```javascript
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

## Ajax

```javascript
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

