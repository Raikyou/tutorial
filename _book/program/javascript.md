

### Javasript

```javascript
//输出
document.write("<h1>This is a heading</h1>");           //写入html输出
document.getElementById("demo").innerHTML="Hello JavaScript";          //查找html元素并改变其内容
document.getElementById("demo").style.color="#ff0000";        //查找html元素并改变其样式

//语句
var name="Hello"; var name = "Hello";     //JS忽略脚本中的空格，“;”用来分隔语句和在同一行写多条语句，“;”是可选的
document.write("hello \                        
world");                                         //在文本字符串中使用\来实现换行
//变量
var x=2, y=x+1, z="string";               //声明变量并赋值,","用以分隔变量，也可以多行书写
var x;                                   //未赋值的变量值统一为undefined
var x=2; var x;                         //重新声明后x的值仍为2
//数据类型：字符串string、数字number、布尔boolean、数组array、对象object、Null、Undefined
var a=true， b=false;           //布尔逻辑值
var cars=new Array();           //通过new声明变量类型为数组
cars[0]="Audi";
cars[1]="BMW";
cars[2]="Volvo";
var cars=new Array("Audi","BMW","Volvo");    
var cars=["Audi","BMW","Volvo"];                           
var person={firstname:"Bill", lastname:"Gates", id:5566};   //对象属性以name:value来定义，对象有属性和方法
objectName.popertyName         //访问对象属性
objectName.methodName          //访问对象方法

```
