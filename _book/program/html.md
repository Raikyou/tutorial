
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
