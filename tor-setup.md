# Setting up a tor relay
### 安装过程
 方法一：通过包管理工具安装
``` shell
# on Debian
apt update
apt install tor
```
方法二： 自源码编译
1) 安装依赖 ``` libevent openssl zlib```
``` shell
apt install libevent-dev openssl zlib1g zlib1g-dev
```
2) 从官网[下载源代码包][1]或者从GIt仓库克隆得到源代码
``` shell
git clone https://git.torproject.org/tor.git
```
3) 解压/克隆完成后进入项目根目录执行
``` shell
./configure && make
```
4) 进入 ```src/or/``` 目录执行 ```./tor``` 即可按默认设置启动Tor
5) 想要安装的话执行 ```make install``` 即可

### Tor配置
修改```torrc```文件，该文件的位置

> Otherwise, if you are using Tor without Tor Browser, it looks for the torrc file in ```/usr/local/etc/tor/torrc``` if you compiled tor from source, and ```/etc/tor/torrc``` or ```/etc/torrc``` if you installed a pre-built package.

根据安装方式（包管理/源码编译）不同，配置文件位置不同。

配置项说明

>鸽了鸽了



  [1]: https://www.torproject.org/download/download