# BBR

## Installation

```bash
sudo wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh 
chmod +x bbr.sh && ./bbr.sh
# restart after installation
```

## Vertification

`lsmod | grep bbr`

Succeeded If returning `tcp_bbr` .

