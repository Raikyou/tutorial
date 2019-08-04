# Internet Protocol

## Physical layer

光缆、电缆等，负责传送0和1的电信号

## Link layer

确定0和1的分组方式

* Ethernet Protocol: Head\(18 bytes\) + Data\(46 - 1500 bytes\)

## Network layer

* IP Protocol:
* * 静态IP
  * 动态IP: 需要DHCP协议\(应用层\)分配IP地址和相关网络参数

IP 地址分为网络部分和主机部分，网络部分相同则处于同一子网络中

根据子网掩码可以分辨网络部分，它的网络部分全为1，主机部分全为0，如255.255.255.0

## Transport layer

端口对端口的传输

* UDP：不需要确认数据包接收
* TCP：需要确认数据包接收

## Application layer

规定应用程序的数据格式，如Email、WWW、FTP

![](https://github.com/Raikyou/tutorial/tree/23b49471dc8b87fabbe4cb1d691f37e3cd390b8a/tech/.gitbook/assets/image.png)

