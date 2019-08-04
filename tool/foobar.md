# Foobar

## 代码

```text
$sub(%_height%,xx) = 面板高度- xx
$sub(%_width%,xx) = 面板高度- xx
%ps_height% 高度
```

## 标签格式

在“显示/DUI”的窗口标题中写入

```text
[%artist%][ - %title% ] #若方括号内的标签信息存在则显示，否则不显示
```

## 组件

* 分栏用户界面：foo\_ui\_columns.dll
* APE解码：foo\_input\_monkey.dll
* 批量修改标签：foo\_masstag.dll
* 批量修改文件名：foo\_fileops.dll（文件名模板：%artist% - %title%）

封面显示

在“显示/分栏用户界面”粘贴一下内容

* 专辑

```text
$replace(%path%,%filename_ext.%,cover.*p*g)
$replace(%path%,%filename_ext.%,folder.*p*g)
$replace(%path%,%filename_ext%,*front.*p*g)
```

* 歌手

```text
$replace(%path%,%filename_ext.%,cover.*p*g)
$replace(%path%,%filename_ext.%,folder.*p*g)
$replace(%path%,%filename_ext%,*front.*p*g)
```

## Foobar个人设置

* 媒体库：添加音乐路径
* 外壳交互：文件关联（ape, flac, mp3, cue, tak，绿色版关联在根目录下必须有shellext64.dll和foobar2000 Shell Associations Updater，同时删除portable\_mode\_enabled），勾选“在启动时注册支持的文件格式”和“总是发送文件到播放列表”

