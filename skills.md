# Skills

## Rename in

### Suffix

进入Command Line窗口文件夹下，输入`ren *.html *.txt`

### PowerShell

1. 切換至檔案所在目錄後，使用 `Dir` 指令將所有的檔案名稱列出來，然後交給 `Rename-Item` 指令進行更改檔名的動作。

       `Dir | Rename-Item -NewName { $_.name -replace " ", "-" }`

        该命令可将文件名中的空格替换为 "-" 

2. 把所有的 jpg 圖檔重新命名為 `image_編號.jpg`，而編號的起始數字可以自己設定：

```text
# 把所有的 JPG 檔案重新命名為 image_num.jpg
Get-ChildItem *.jpg | ForEach-Object -Begin {
  $count = 1
} -Process {
  Rename-Item $_ -NewName "image_$count.jpg"
  $count++
}
```

 從所有的 `*.jpg` 檔案中，找出含有 `oldstring` 字眼的檔案，然後把 `oldstring` 這個字眼全部改為 `newstring`：

```text
# 從所有的 *.jpg 檔案中，找出含有 oldstring 字眼的檔案，
# 把 oldstring 改為 newstring
Get-ChildItem *.jpg -Filter "*oldstring*" | ForEach {
  Rename-Item $_ -NewName $_.Name.Replace("oldstring","newstring")
}
```

