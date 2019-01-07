## SSR

### Install

```bash
git clone -b manyuser https://github.com/Raikyou/shadowsocksr
cd shadowsocksr
bash initcfg.sh
vi user-config.json
cd shadowsocks
./logrun.sh
```

### Config

```javascript
// single user
"server_port": 8388,
"password": "m",
"method": "rc4-md5",
"protocol": "auth_aes128_md5",
"obfs": "tls1.2_ticket_auth",

// only ports and password
"port_password":{
        "80":"password1",
        "443":"password2"
        },

 // all paras   
"port_password":{
        "8388":{"protocol":"auth_simple", "password":"abc", "obfs":"plain", "obfs_param":""},
        "8389":{"protocol":"origin", "password":"abcde"}
        },
```

### Startup

```bash
chmod +x /etc/rc.local
vi etc/rc.local
# add '/bin/bash /root/shadowsocksr/shadowsocks/logrun.sh'
```

### Update

```bash
cd shadowsocksr
git pull
# restart after succeeding
```

**Reference**

* [ShadowsocksR 服务端安装教程](https://github.com/Ssrbackup/shadowsocks-rss/wiki/Server-Setup)
* [ShadowsocksR 单用户版服务端安装教程](https://doub.io/ss-jc11/)

## BBR

```bash
sudo wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh 
chmod +x bbr.sh && ./bbr.sh
# restart after installation
lsmod | grep bbr    # Succeeded If returning tcp_bbr
```



