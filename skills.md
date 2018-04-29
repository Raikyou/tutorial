# Skills

## Rename in Explorer

### Command Prompt

```bash
# rename suffix
ren *.jpg *.png
```

### PowerShell

{% code-tabs %}
{% code-tabs-item title="replace" %}
```bash
# replace " " with "-"
Dir | Rename-Item -NewName { $_.name -replace " ", "-" }
```
{% endcode-tabs-item %}

{% code-tabs-item title="sort" %}
```bash
# rename *.JPG to image_num.jpg
Get-ChildItem *.jpg | ForEach-Object -Begin {
  $count = 1
} -Process {
  Rename-Item $_ -NewName "image_$count.jpg"
  $count++
}
```
{% endcode-tabs-item %}

{% code-tabs-item title="string" %}
```bash
# find and replace "oldstring" to "newstring" 
Get-ChildItem *.jpg -Filter "*oldstring*" | ForEach {
  Rename-Item $_ -NewName $_.Name.Replace("oldstring","newstring")
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

**Reference**

* [在 Windows 中更改大量檔案名稱，批次修改檔名，快速又省力！](https://blog.gtwang.org/windows/how-to-batch-rename-files-in-windows/)
* [Windows PowerShell 使用教學課程](https://msdn.microsoft.com/zh-tw/library/ee790872%28v=azure.10%29.aspx)



