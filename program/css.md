# css

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
    text-decoration: line-through;        /*删除线*/
    text-indent: 2em;                     /*首行缩进*/
    line-height: 2em;                     /*行间距*/
    letter-spacing: 50px;                 /*字母间距*/
    word-spacing: 50px;                   /*单词间距*/
}
li strong              /*后代选择器,所有后代*/
li > strong            /*子元素选择器，直接后代*/
h1 + p                 /*兄弟选择器，紧邻在h1后面的所有p元素*/
#id 
.class
```

