---
description: python
---

# SSR

## Installation

{% code-tabs %}
{% code-tabs-item title="Installation" %}
```bash
git clone -b manyuser https://github.com/Raikyou/shadowsocksr`
cd shadowsocksr
bash initcfg.sh
vi user-config.json
cd shadowsocks
./logrun.sh  # stop.sh & tail.sh
```
{% endcode-tabs-item %}

{% code-tabs-item title="Configuration" %}
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
{% endcode-tabs-item %}

{% code-tabs-item title="Multi-user" %}
```javascript

```
{% endcode-tabs-item %}

{% code-tabs-item title="Run in version of github" %}
```bash
python server.py        # run in the foregroung
# mainly used for debugging，truned off after disconnecting SSH）
python server.py -d start        # run in the background
python server.py -d stop/restart        # stop or restart
tail -f /var/log/shadowsockr.log        # view the log
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Start up

{% code-tabs %}
{% code-tabs-item title="Debian" %}
```bash
chmod +x /etc/rc.local
vi etc/rc.local
# add '/bin/bash /root/shadowsocksr/shadowsocks/logrun.sh' before 'exit 0'
```
{% endcode-tabs-item %}

{% code-tabs-item title="Cent OS" %}
```bash
chmod +x /etc/rc.d/rc.local
vi /etc/rc.d/rc.local
/bin/bash
# add '/bin/bash /root/shadowsocksr/shadowsocks/logrun.sh'
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Update

```bash
cd shadowsocksr
git pull
# restart after succeeding
```

## Reference

\[1\] [ShadowsocksR服务端安装教程](https://github.com/Ssrbackup/shadowsocks-rss/wiki/Server-Setup)

\[2\] [ShadowsocksR 单用户版服务端安装教程](https://doub.io/ss-jc11/)



