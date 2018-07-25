# 前言说明

各平台变量

| Platform | Name | User Path |
| :--- | :--- | :--- |
| Linux | 中州韵 ibus-rime | ~/.config/ibus/rime |
| OSX | 鼠须管 squirrel | ~/Library/Rime |
| Windows | 小狼毫 weasel | %APPDATA%Rime |

`User Path` 包含以下内容：

| File | Description |
| :--- | :--- |
| default.custom.yaml | 全局设定 |
| name.custom.yaml | 候选栏设定 |
| luna\_pinyin\_simp.custom.yaml | 输入方案副本（扩充词库、符号等） |
| installation.yaml | 安装信息（同步） |

# 配置方法

### default.custom.yaml

```yaml
# default.custom.yaml
patch:
  menu/page_size: 9           # 设置候选字数量
  schema_list:
    - schema: luna_pinyin_simp
  ascii_composer/good_old_caps_lock: true
  ascii_composer/switch_key:
    Caps_Lock: commit_code
    Shift_L: commit_code
    Shift_R: commit_text
    Control_L: commit_code
    Control_R: commit_code
  switcher/hotkeys:       
    - F4
```

### &lt;name&gt;.custom.yaml

```yaml
# <name>.custom.yaml
patch:
  style
    border_height: 10
    border_width: 10
    corner_radius: 9
    display_tray_icon: false
    font_face: "Nirmala UI"   
    font_point: 12
    label_font_face: "Nirmala UI"  
    horizontal: true
    line_spacing: 10
    color_scheme: simple
  preset_color_schemes/simple:
    name: "简洁／simple"
    author: Raikyou
    back_color: 0x453A32
    border_color: 0xffffff
    text_color: 0xACA59E
    candidate_text_color: 0xACA59E
    comment_text_color: 0xACA59E
    hilited_back_color: 0x453A32
    hilited_candidate_back_color: 0x453A32
    hilited_candidate_text_color: 0xFFFFFF
    hilited_text_color: 0xACA59E
```

### luna\_pinyin\_simp.custom.yaml

```yaml
# luna_pinyin_simp.custom.yaml
patch:
  'punctuator/import_preset': symbols
  'recognizer/patterns/punct': "^/([a-z]+|[0-9])$"
  "translator/dictionary": luna_pinyin.extended              # 載入朙月拼音擴充詞庫
  "speller/algebra/@before 0": xform/^([b-df-np-z])$/$1_/ # 改寫拼寫運算，使含西文的詞彙(luna_pinyin.cn_en.dict.yaml)不影響簡拼功能
```

  
下载 [luna 扩充词库](https://bintray.com/rime-aca/dictionaries/luna_pinyin.dict)并将以下词库移动到 `User Path`

> luna\_pinyin.extended.dict.yaml  
>  luna\_pinyin.hanyu.dict.yaml  
>  luna\_pinyin.poetry.dict.yaml  
>  luna\_pinyin.cn\_en.dict.yaml

若要添加新词库，只需在 `luna_pinyin.extended.dict.yaml` 中添加词库词条

# installation.yaml

```
sync_dir: "~/Dropbox/Rime"
```

# Reference

1. [Rime 定制指南](https://github.com/rime/home/wiki/CustomizationGuide)
2. lonelygo. 2015,1. [Rime输入法—鼠须管\(Squirrel\)词库添加及配置](https://www.jianshu.com/p/cffc0ea094a7)
3. [〔新手推荐敎程〕关于导入词库及「深蓝词库转换」的正确操作方法](https://link.jianshu.com?t=http://tieba.baidu.com/p/2757690418)



