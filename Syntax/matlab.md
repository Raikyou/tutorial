## 1 字符串分割

```
S = regexp(str, char, 'split')
```

Example：

```
str = 'Hello Studio'
S = regexp(str, '\s+', 'split')

S(1)='Hello'
S(2)='Studio'
```

注意，此时 S 是一个 cell 型变量，它的每个元素比如S\(1\)仍然是cell型的，只能用来display，不能直接用来进行字符串操作（比如获取其中的某个字符），所以我们在使用需要执行一次：

```
s1 = char(S(1))
```

这样的s1才是一个真正的字符串，可以进行后续的操作。

## 2 Figure 的 subplot 位置控制

### 2.1 只在最后一个 subplot 右侧显示 colorbar

```
p = get(subplot(2,5,10),'Position');
colorbar('Position', [p(1)+p(3)+gap  p(2)  colorbar_axw  p(4)])
```

### 2.2 自定义 subplot 位置和间距

```
px = px + axw + gap;
py = py - axh - gap;
```

**Reference**

[matlab控制图像的边界（margin），subplot的间距（gap）](https://blog.csdn.net/lanchunhui/article/details/49820721)

