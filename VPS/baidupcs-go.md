### 自动获取最新版本

```
Ver=$(wget --no-check-certificate -qO- https://api.github.com/repos/iikira/BaiduPCS-Go/releases/latest | grep -o '"tag_name": ".*"' | sed 's/"//g' | sed 's/tag_name: //g') && echo ${Ver}
```

### 安装

```
wget --no-check-certificate -O BaiduPCS-Go.zip https://github.com/iikira/BaiduPCS-Go/releases/download/${Ver}/BaiduPCS-Go-${Ver}-linux-amd64.zip

unzip BaiduPCS-Go.zip && rm BaiduPCS-Go.zip

cd BaiduPCS-Go && ./BaiduPCS-Go
```

### 使用

```
BaiduPCS-Go > login                              # 登陆账号
BaiduPCS-Go > updata                             # 检测程序更新
BaiduPCS-Go > config set -max_parallel 500 -savedir ~/downloads               # 设置下载路径和最大并发量
BaiduPCS-Go > d /path/file          # 下载 /path/file 所制定的文件，支持文件夹
```



