### 用golang在树莓派上玩ipfs


### 玩转树莓派，搭好游戏平台

### 树莓派下安装golang

1、下载golang安装包
   ~$ wget https://www.golangtc.com/static/go/1.9.2/go1.9.2.linux-armv6l.tar.gz

2、安装golang
   ~$ sudo tar -xzf go1.9.2.linux-armv6l.tar.gz -C /usr/local

3、配置golang环境
   ~$ sudo nano $HOME/.profile

   在文件中添加下面内容

   export PATH=$PATH:/usr/local/go/bin

   export PATH=$PATH:/usr/local/pi/go/bin

   export PATH=$PATH:/home/pi/go/bin

   export GOPATH=/home/pi/go

   按ctrl + X 键保存退出

   运行一下命令，使配置生效

   ~$ source $HOME/.profile

   测试一下golang是否装好，输入以下命令：
   
   ~$go env
   
   如果看到显示输出正常，则golang安装完毕

##深入学习golang


###理解blockchain

### 重要提示
由于有墙，国内无法连接www.golang.org。所有golang.org的包在github.com有托管。可用如下方法获得。

golang.org/x/xxx 包的手动安装方法：

golang.org/x/xxx 这类包托管在 github.com/golang，从这里找到相应的包即可。比如 golang.org/x/crypto 包的安装，找到对应的地址为： https://github.com/golang/crypto ，运行以下命令：

$ cd $GOPATH/src

$ mkdir golang.org

$ cd golang.org

$ mkdir x

$ cd x

$ git clone https://github.com/golang/crypto.git




##Installing with ipfs-update

ipfs-update is a command-line tool to install and upgrade the ipfs binary.

Getting ipfs-update

ipfs-update can be downloaded for your platform at: https://dist.ipfs.io/#ipfs-update

If you have a working Go environment (>=1.8), you can also install it with: go get -u github.com/ipfs/ipfs-update.

When installing new versions of ipfs or upgrading make sure you are using the latest version of ipfs-update.

Installing ipfs with ipfs-update

ipfs-update versions lists all the available ipfs versions which are available for download:

$ ipfs-update versions

v0.3.2

v0.3.4

v0.3.5

v0.3.6

v0.3.7

v0.3.8

v0.3.9

v0.3.10

v0.3.11

v0.4.0

v0.4.1

v0.4.2

v0.4.3

v0.4.4

v0.4.5

v0.4.6

v0.4.7-rc1

ipfs-update install latest will install the latest available version:

$ ipfs-update install latest

fetching go-ipfs version v0.4.7-rc1

binary downloaded, verifying...

success!

stashing old binary

installing new binary to /home/hector/go/bin/ipfs

checking if repo migration is needed...

Installation complete!

Note that the latest available version may not be stable (i.e. release candidates in the form vX.X.X-rcX). So it is recommended to specify the version you want to install, for example: ipfs-update install v0.4.6.

