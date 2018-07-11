

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
