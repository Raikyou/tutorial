# BaiduPCS-Go

## Installation

```bash
Ver=$(wget --no-check-certificate -qO- https://api.github.com/repos/iikira/BaiduPCS-Go/releases/latest | grep -o '"tag_name": ".*"' | sed 's/"//g' | sed 's/tag_name: //g') && echo ${Ver}
wget --no-check-certificate -O BaiduPCS-Go.zip https://github.com/iikira/BaiduPCS-Go/releases/download/${Ver}/BaiduPCS-Go-${Ver}-linux-amd64.zip
unzip BaiduPCS-Go.zip && rm BaiduPCS-Go.zip
cd BaiduPCS-Go && ./BaiduPCS-Go
```

## Usage

```text
BaiduPCS-Go > login                              
BaiduPCS-Go > updata                            
BaiduPCS-Go > config set -max_parallel=500 -savedir /usr/local/caddy/www/aria2/Download   
BaiduPCS-Go > d /path/file
```

 **Referrence** 

* [BaiduPcs-web](https://github.com/liuzhuoling2011/baidupcs-web) from _liuzhuoling2011_
* [BaiduPcs-Go](https://github.com/iikira/BaiduPCS-Go\) from _iikira_

