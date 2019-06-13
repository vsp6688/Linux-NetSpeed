# Linux-NetSpeed 
超级一键加速脚本，bbr 原版/魔改/plus/锐速 四合一
前言：
很多时候，我们为了给VPS加速，会选择不同的方式，比如BBR、锐速等，但单独BBR目前就有普通版、魔改版和plus版，加上锐速，无疑需要很多的脚本，这样在安装上也非常的不方便，而最近，loc论坛的网友又发挥了超人的实力，整出了一个集合BBR、BBR魔改、BBR plus、锐速四合一的脚本，给我们安装提供了极大的方便。

项目地址：
https://github.com/cx9208/Linux-NetSpeed
简介：

本脚本支持KVM架构的VPS，不支持OpenVZ，
在vultr上 Centos 7, Debian 8/9, Ubuntu 16/18测试通过
安装命令：

wget "https://github.com/chiakge/Linux-NetSpeed/raw/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
部分如果提示连接不上github。可以先安装
yum install net-tools -y  或者 apt-get install net-tools -y

如果没有wget，比如搬瓦工vps，可以先安装wget

yum -y install wget
执行如何提示证书错误的话

yum -y install ca-certificates
或者

apt-get -y install ca-certificates
说明：
1. 先在[1 - 3]切换内核（第一次显示为bbr内核也要切换一遍），重启
出现这个选no
超级一键加速脚本，bbr 原版/魔改/plus/锐速 四合一

2. 重启后不用再下载脚本，直接 ./tcp.sh ，在[4 - 8]中选你要开的加速
"1. 安装 BBR/BBR魔改版内核"        对应4,5,6（原版，魔改，暴力魔改）
"2. 安装 BBRplus版内核 "                对应7（plus）
"3. 安装 Lotserver(锐速)内核"        对应8（锐速）

3. 开启后再 ./tcp.sh  ， 显示开启成功则启动成功，你也可以自己手动确认
