# Linux

## 主要发行版本
- Ubuntu
- CentOS
- RedHat
- Debian
- Fedora
- SuSE
- OpenSUSE
- Arch Linux
- SolusOS

本文主要以 CentOS 为例。

## 安装

CentOS 下载地址：  
https://www.centos.org/download/

VMware 安装 Centos7 超详细过程点击[这里](https://www.runoob.com/w3cnote/vmware-install-centos7.html)

## 系统目录结构
Linux 有且只有一个根目录。

- /bin   
  bin 是 Binaries (二进制文件) 的缩写, 这个目录存放着最经常使用的命令。

- /boot  
  这里存放的是启动 Linux 时使用的一些核心文件，包括一些连接文件以及镜像文件。

- /dev  
  dev 是 Device(设备) 的缩写, 该目录下存放的是 Linux 的外部设备，在 Linux 中访问设备的方式和访问文件的方式是相同的。

- /etc  
  etc 是 Etcetera(等等) 的缩写,这个目录用来存放所有的系统管理所需要的配置文件和子目录。

- /home  
  用户的主目录

- /lib  
  lib 是 Library(库) 的缩写这个目录里存放着系统最基本的动态连接共享库，其作用类似于 Windows 里的 DLL 文件。几乎所有的应用程序都需要用到这些共享库。

- /lost+found  
  这个目录一般情况下是空的，当系统非法关机后，这里就存放了一些文件。

- /media 
  linux 系统会自动识别一些设备，例如U盘、光驱等等，当识别后，Linux 会把识别的设备挂载到这个目录下。

- /mnt  
  系统提供该目录是为了让用户临时挂载别的文件系统的，我们可以将光驱挂载在 /mnt/ 上，然后进入该目录就可以查看光驱里的内容了。

- /opt  
  opt 是 optional(可选) 的缩写，这是给主机额外安装软件所摆放的目录。比如你安装一个ORACLE数据库则就可以放到这个目录下。默认是空的。

- /proc  
  这是一个虚拟的目录，它是系统内存的映射，访问这个目录来获取系统信息。

- /root  
  该目录为系统管理员，也称作超级权限者的用户主目录。

- /sbin  
  这里存放的是系统管理员使用的系统管理程序

- /selinux  
  这个目录是 Redhat/CentOS 所特有的目录，Selinux 是一个安全机制，类似于 windows 的防火墙，但是这套机制比较复杂，这个目录就是存放selinux相关的文件的。

- /srv  
  该目录存放一些服务启动之后需要提取的数据。

- /sys  
  这是 Linux2.6 内核的一个很大的变化。该目录下安装了 2.6 内核中新出现的一个文件系统 sysfs 。

- /tmp  
  tmp 是 temporary(临时) 的缩写这个目录是用来存放一些临时文件的。

- /usr  
  usr 是 unix shared resources(共享资源) 的缩写，这是一个非常重要的目录，用户的很多应用程序和文件都放在这个目录下，类似于 windows 下的 program files 目录。

- /usr/local  
  给主机额外安装软件所安装的目录，一般是通过编译源码方式安装的程序。

- /var  
  这个目录中存放着在不断扩充着的东西，习惯将那些经常被修改的目录放在这个目录下。包括各种日志文件。

- /run  
  是一个临时文件系统，存储系统启动以来的信息。当系统重启时，这个目录下的文件应该被删掉或清除。如果你的系统上有 /var/run 目录，应该让它指向 run。

