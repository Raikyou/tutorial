# Caddy & Aria2 & Cloud

## 1. Caddy FileManager

```text
wget -N --no-check-certificate https://softs.loan/Bash/caddy_install.sh 
bash caddy_install.sh install http.filemanager
mkdir /usr/local/caddy/www && mkdir /usr/local/caddy/www/aria2
```

```text
echo ":80 {
 root /usr/local/caddy/www/aria2
 timeouts none
 gzip
 filemanager /Download /usr/local/caddy/www/aria2/Download {
  database /usr/local/caddy/filemanager.db
 }
}" > /usr/local/caddy/Caddyfile
```

## 2. Aria2 后端

```text
wget -N --no-check-certificate https://softs.loan/Bash/aria2.sh && bash aria2.sh
```

下载目录 `/usr/local/caddy/www/aria2/Download`

## 3. Aria2 前端

```text
mkdir /usr/local/caddy/www/aria2/Download && cd /usr/local/caddy/www/aria2
Ver=$(wget --no-check-certificate -qO- https://api.github.com/repos/mayswind/AriaNg/releases/latest | grep -o '"tag_name": ".*"' | sed 's/"//g' | sed 's/tag_name: //g') && echo ${Ver} 
wget -N --no-check-certificate "https://github.com/mayswind/AriaNg/releases/download/${Ver}/aria-ng-${Ver}.zip"
unzip aria-ng-${Ver}.zip && rm -rf aria-ng-${Ver}.zip
```

