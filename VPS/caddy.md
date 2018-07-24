## 1. Aria2 后端

```
wget -N --no-check-certificate https://softs.loan/Bash/aria2.sh 

bash aria2.sh
```

下载目录 `/usr/local/caddy/www/aria2/Download`

## 2. Caddy FileManager

## 安装

```
wget -N --no-check-certificate https://softs.loan/Bash/caddy_install.sh 

bash caddy_install.sh install http.filemanager
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

### 创建文件夹

```
mkdir /usr/local/caddy/www/aria2/Download && cd /usr/local/caddy/www/aria2
```

### 自动获取最新版本号

```
Ver=$(wget --no-check-certificate -qO- https://api.github.com/repos/mayswind/AriaNg/releases/latest | grep -o '"tag_name": ".*"' | sed 's/"//g' | sed 's/tag_name: //g') && echo ${Ver}
```

### 安装

```
wget -N --no-check-certificate "https://github.com/mayswind/AriaNg/releases/download/${Ver}/aria-ng-${Ver}.zip"

unzip aria-ng-${Ver}.zip

rm -rf aria-ng-${Ver}.zip
```

## 4. Cloud Torrent

### 安装

```
wget -N --no-check-certificate https://softs.loan/Bash/cloudt.sh 

bash cloudt.sh
```

## 5. Transmission

### 安装

```
apt-get install -y transmission-daemon
```

### 配置

```

/etc/init.d/transmission-daemon stop

vim /var/lib/transmission-daemon/info/settings.json

/etc/init.d/transmission-daemon start
```

### 美化

```
wget --no-check-certificate https://github.com/ronggang/transmission-web-control/raw/master/release/install-tr-control.sh

bash install-tr-control.sh
```


