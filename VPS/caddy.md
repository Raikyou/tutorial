## 1. Aria2 后端

```
wget -N --no-check-certificate https://softs.loan/Bash/aria2.sh && chmod +x aria2.sh && bash aria2.sh
```

下载目录 `/usr/local/caddy/www/aria2/Download`

## 2. Caddy FileManager

## 安装

```
wget -N --no-check-certificate https://softs.loan/Bash/caddy_install.sh && chmod +x caddy_install.sh && bash caddy_install.sh install http.filemanager
```

### 创建文件夹

```
mkdir /usr/local/caddy/www && mkdir /usr/local/caddy/www/aria2
```

### 配置

```
echo ":80 {
 root /usr/local/caddy/www/aria2
 timeouts none
 gzip
 filemanager /Download /usr/local/caddy/www/aria2/Download {
  database /usr/local/caddy/filemanager.db
 }
}" > /usr/local/caddy/Caddyfile
```

### 更新

```
bash caddy_install.sh install http.filemanager
```

### 卸载

```
bash caddy_install.sh uninstall
```

## 3. Aria2 前端

```
mkdir /usr/local/caddy/www/aria2/Download && cd /usr/local/caddy/www/aria2

Ver=$(wget --no-check-certificate -qO- https://api.github.com/repos/mayswind/AriaNg/releases/latest | grep -o '"tag_name": ".*"' | sed 's/"//g' | sed 's/tag_name: //g') && echo ${Ver}
```

## 



