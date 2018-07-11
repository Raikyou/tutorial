
### HTML

```html
<!DOCTYPE html>
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
        <title>html语法学习</title>
        <!--外部JavaScript-->
        <script src="url"></script>
        <!--内部JavaScript,也可放在body最后-->
        <script>alert("My First JavaScript");</script>
        <!--外部样式表-->
        <link rel="stylesheet" type="text/css" href="url" />  
        <!--内部样式表-->
        <style type="text/css"> 
            h1 {color: red}
        </style>
    </head>
    <!--主体部分-->
    <body bgcolor="red" background="url">
        <h1 align="center">headline</h1>
        <!--内联样式-->
        <p style="color:red; margin-left:20px">paragraph</p>
        <a href="url" target="_blank">text</a>
        <a name="label">anchor</a>
        <a href="#laber">anchor</a>
        <a href="mailto:xxx@gmail.com?cc=xxx.gmail.com&title=xxx&body=xxx">联系邮箱</a>
        <img src="url" width="200" height="200" alt="image" title="图片" align="bottom" usemap="#mapname" />
        <map name="mapname" id="mapname"><area shape="circle" coords="x,y,z,r" href="url"></map>
        <table border="1" cellpadding="10" cellspacing="5">
            <caption>headline</caption>
            <tr><td></td></tr>
        </table>
        <ul><ol><li></li></ol></ul>
        <!--表单-->
        <form method="get/post" action="save.php">
            <label for="idname"> xx </label>
            <input type="text" name="myname" />
            <input type="password" name="pass" />
            <input type="submit" name="submit" value="确定" />
            <input type="reset" name="reset" value="重置" />
            <input type="radio/checkbox" name=radioname" value="选项值" checked="checked" /> <!--同一组单选按钮name必须相同-->
            <select>
                <option value="提交值" selected="selected">显示下拉值</option>
            </select>>
            <textarea rows="10" cols="10">请在此输入内容</textarea>
        </form>
    </body>
</html>


```

### CSS

```css
/*选择器分组*/
h1,h2,h3 {
    color: red;
    border: 1px solid #000;
    padding: 10px 10px 20px 20px;
    margin: 10px;
    font-family: "Microsoft Yahei"；
    font-size: 14px;
    font-weight: bold;
    font-style: italic;
    text-align: center;
    text-decoration: underline;            
    text-decoration: line-through;        /*删除线*/
    text-indent: 2em;                     /*首行缩进*/
    line-height: 2em;                     /*行间距*/
    letter-spacing: 50px;                 /*字母间距*/
    word-spacing: 50px;                   /*单词间距*/
}
li strong 
li>strong
#id 
.class 

```

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

### Python

```python
#Python大小写敏感
name=input('please enter your name:')
print('hello',name)  #也可以用","连接不通字符串'hellp','world'
print('''line1
    line2
    line3''') 

#列表list的查找、插入、删除、替换
person=['michael','bob','tracy']   #list数据类型
len(person)       #输出list元素的个数,输出结果为3
person[0]      #输出第一个元素，也可以写成person[-3]表示输出第三个元素
person.append('adam')    #插入元素到最后一个位置
person.insert(1,'jack')    #插入到第2个位置
person.pop(1)  #删除第2个元素，括号内无数字则删除最后一个元素
person[1]='sarah'  #将第2个元素替换为'sarah'
#元组tuple只可查找，不能更改内部元素
person=('michael','bob','tracy')

#dict内部顺序与key放入顺序无关，且key必须是不可变的，因此不能用list
person = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
>>> person['Michael']          #输出michael对应的value
95
>>> 'Thomas' in perspn     #判断thomas是否在person中      
False
>>> d.get('Thomas')        #判断thomas是否在person中并返回none或指定值
>>> d.get('Thomas', -1)
-1

#set：一组key的集合，无序，只显示包含的无重复元素
s1 = set([1, 1, 2, 2, 3, 3])
print(s1)                   #输出{1, 2, 3}
s2 = set([2, 3, 4])
print(s1 & s2)               #交集{2, 3}
print(s1 | s2)              #并集{1, 2, 3, 4}

#if语句
age=3
if age>=18:
    print('adult')
elif age>=6:
    print('teenager')
else:
    print('kid')

#for...in循环
sum=0                  
for x in range(101):    #range(101)生成0-100的整数序列
    sum=sum+x
print(sum)               #0到100的整数之和
#while循环
sum=0
n=99
while n>0:
    sum=sum+n
    n=n-2
print(sum)

#函数
def function(x,y=3):  #x必选参数，y默认参数 
    pass
def calc(*numbers):    #可变参数，调用为calc(1, 2)；若定义为calc(numbers)，则调用为calc([1, 2])
    sum = 0
    for n in numbers:
        sum = sum + n * n
    return sum
def person(name, age, **kw):    #关键字参数，可以输入，也可以不输入
    print('name:', name, 'age:', age, 'other:', kw)

#切片
l(0:10:2)  #取list或tuple的前10个数，每2个取一个
l(-2:)    #取倒数第2个数和倒数第1个数
#列表生成器
[x*x for x in range(1,11) if x%2==0]   #生成1-10之间偶数平方的列表[4, 16, 36, 64, 100]
[s.lower() for s in ['Abc', 'dE', 18, 'fg'] if isinstance(s,str)]  #将列表内字符串转化为小写['abc', 'de', 'fg']
#生成器
#方法1:用[]生成列表，用（）生成iterator
  g = (x * x for x in range(10))   
  #方法2:用print x顺序执行，遇到return返回，用yield x生成iterator并返回 
  yield x                           
  #调用iterator
  next(g)     #每次只返回一个值
  for n in g       #返回iterator所有值
    print(n)   

```

### Markdown

| `# H1` | # H1 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `** Bold **` | **Bold** |
| `_Italic_` | _Italic_ |
| `~~strikethrough~~` | ~~strikethrough~~ |
| `1. order` | 1. order |
| `- bullet order` | - bullet order |
| `[google link](https://www.google.com 'google homepage')` | [google link](https://www.google.com) |
| `![page icon](url 'gitbook icon')` | ![githook icon](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/spaces%2F-L9tpLefuy10oQDBjWcS%2Favatar.png?generation=1523545518862026&alt=media) |

Reference

* [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)
* [https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

