# Linux
Linux 内核最初只是由芬兰人林纳斯·托瓦兹（Linus Torvalds）在赫尔辛基大学上学时出于个人爱好而编写的。  
Linux 是一套免费使用和自由传播的类 Unix 操作系统，是一个基于 POSIX 和 UNIX 的多用户、多任务、支持多线程和多 CPU 的操作系统。  
Linux 能运行主要的 UNIX 工具软件、应用程序和网络协议。它支持 32 位和 64 位硬件。Linux 继承了 Unix 以网络为核心的设计思想，是一个性能稳定的多用户网络操作系统。
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

## 常用命令

### ls 命令

就是 list 的缩写，通过 ls 命令不仅可以查看 linux 文件夹包含的文件，而且可以查看文件权限(包括目录、文件夹、文件权限)查看目录信息等等。

> ls -a 列出目录所有文件，包含以.开始的隐藏文件  
> ls -A 列出除.及..的其它文件  
> ls -r 反序排列   
> ls -t 以文件修改时间排序  
> ls -S 以文件大小排序  
> ls -h 以易读大小显示  
> ls -l 除了文件名之外，还将文件的权限、所有者、文件大小等信息详细列出来  

### cd 命令

Linux cd（英文全拼：change directory）命令用于切换当前工作目录。

> cd [目录名]  

### pwd 命令

pwd 命令用于查看当前工作目录路径。

实例：

(1) 查看当前路径
> pwd  

(2) 查看软链接的实际路径
> pwd -P

### mkdir 命令

mkdir 命令用于创建文件夹。

> mkdir [-p] dirName

可用选项：
- -m: 对新建目录设置存取权限，也可以用 chmod 命令设置;
- -p: 可以是一个路径名称。此时若路径中的某些目录尚不存在,加上此选项后，系统将自动建立好那些尚不在的目录，即一次可以建立多个目录。

### rm 命令

删除一个目录中的一个或多个文件或目录，如果没有使用 -r 选项，则 rm 不会删除目录。如果使用 rm 来删除文件，通常仍可以将该文件恢复原状。

> rm [选项] 文件…

选项：
- -i 删除前逐一询问确认。
- -f 即使原档案属性设为唯读，亦直接删除，无需逐一确认。
- -r 将目录及以下之档案亦逐一删除。

实例：

```sh
# rm  test.txt 
rm：是否删除 一般文件 "test.txt"? y  
# rm  homework  
rm: 无法删除目录"homework": 是一个目录  
# rm  -r  homework  
rm：是否删除 目录 "homework"? y 
# rm -rf test
删除 test 子目录及子目录中所有档案删除，并且不用一一确认
```

### rmdir 命令

从一个目录中删除一个或多个子目录项，删除某目录时也必须具有对其父目录的写权限。
> rmdir [-p] dirName

参数：
- -p 是当子目录被删除后使它也成为空目录的话，则顺便一并删除。

实例:
```sh
# 将工作目录下，名为 AAA 的子目录删除
rmdir AAA
```

### mv 命令

mv（英文全拼：move file）命令用来为文件或目录改名、或将文件或目录移入其它位置。

语法：
> mv [options] source dest   
> mv [options] source... directory

参数说明：
- -b: 当目标文件或目录存在时，在执行覆盖前，会为其创建一个备份。
- -i: 如果指定移动的源目录或文件与目标的目录或文件同名，则会先询问是否覆盖旧文件，输入 y 表示直接覆盖，输入 n 表示取消该操作。
- -f: 如果指定移动的源目录或文件与目标的目录或文件同名，不会询问，直接覆盖旧文件。
- -n: 不要覆盖任何已存在的文件或目录。
- -u：当源文件比目标文件新或者目标文件不存在时，才执行移动操作。

实例：
```sh
# 将文件 aaa 改名为 bbb :
mv aaa bbb

# 将 info 目录放入 logs 目录中。注意，如果 logs 目录不存在，则该命令将 info 改名为 logs。
mv info/ logs 

# 再如将 /usr/runoob 下的所有文件和目录移到当前目录下，命令行为：
mv /usr/runoob/*  . 
```

### cp 命令
cp（英文全拼：copy file）命令主要用于复制文件或目录。

语法:
> cp [options] source dest  
> cp [options] source... directory

参数说明：
- -a：此选项通常在复制目录时使用，它保留链接、文件属性，并复制目录下的所有内容。其作用等于dpR参数组合。
- -d：复制时保留链接。这里所说的链接相当于 Windows 系统中的快捷方式。
- -f：覆盖已经存在的目标文件而不给出提示。
- -i：与 -f 选项相反，在覆盖目标文件之前给出提示，要求用户确认是否覆盖，回答 y 时目标文件将被覆盖。
- -p：除复制文件的内容外，还把修改时间和访问权限也复制到新文件中。
- -r：若给出的源文件是一个目录文件，此时将复制该目录下所有的子目录和文件。
- -l：不复制文件，只是生成链接文件。

实例:
```sh
# 使用指令 cp 将当前目录 test/ 下的所有文件复制到新目录 newtest 下，输入如下命令：
cp –r test/ newtest
```
### cat 命令
cat（英文全拼：concatenate）命令用于连接文件并打印到标准输出设备上。

语法:

> cat [-AbeEnstTuv] [--help] [--version] fileName

参数：

- -n 或 --number：由 1 开始对所有输出的行数编号。
- -b 或 --number-nonblank：和 -n 相似，只不过对于空白行不编号。
- -s 或 --squeeze-blank：当遇到有连续两行以上的空白行，就代换为一行的空白行。
- -v 或 --show-nonprinting：使用 ^ 和 M- 符号，除了 LFD 和 TAB 之外。
- -E 或 --show-ends : 在每行结束处显示 $。
- -T 或 --show-tabs: 将 TAB 字符显示为 ^I。
- -A, --show-all：等价于 -vET。
- -e：等价于"-vE"选项；
- -t：等价于"-vT"选项；

实例：
```sh
# 把 textfile1 的文档内容加上行号后输入 textfile2 这个文档里：
cat -n textfile1 > textfile2

# 把 textfile1 和 textfile2 的文档内容加上行号（空白行不加）之后将内容附加到 textfile3 文档里：
cat -b textfile1 textfile2 >> textfile3

# 清空 /etc/test.txt 文档内容：
cat /dev/null > /etc/test.txt
```

### more 命令
more 命令类似 cat ，不过会以一页一页的形式显示，更方便使用者逐页阅读，而最基本的指令就是按空白键（space）就往下一页显示，按 b 键就会往回（back）一页显示，而且还有搜寻字串的功能（与 vi 相似），使用中的说明文件，请按 h 。

语法:
> more [-dlfpcsu] [-num] [+/pattern] [+linenum] [fileNames..]

参数:
- -num 一次显示的行数
- -d 提示使用者，在画面下方显示 [Press space to continue, 'q' to quit.] ，如果使用者按错键，则会显示 [Press 'h' for instructions.] 而不是 '哔' 声
- -l 取消遇见特殊字元 ^L（送纸字元）时会暂停的功能
- -f 计算行数时，以实际上的行数，而非自动换行过后的行数（有些单行字数太长的会被扩展为两行或两行以上）
- -p 不以卷动的方式显示每一页，而是先清除萤幕后再显示内容
- -c 跟 -p 相似，不同的是先显示内容再清除其他旧资料
- -s 当遇到有连续两行以上的空白行，就代换为一行的空白行
- -u 不显示下引号 （根据环境变数 TERM 指定的 terminal 而有所不同）
- +/pattern 在每个文档显示前搜寻该字串（pattern），然后从该字串之后开始显示
- +num 从第 num 行开始显示
- fileNames 欲显示内容的文档，可为复数个数

实例:
```sh
# 逐页显示 testfile 文档内容，如有连续两行以上空白行则以一行空白行显示。
$ more -s testfile

# 从第 20 行开始显示 testfile 之文档内容。
$ more +20 testfile
```

常用操作命令:
- Enter 向下n行，需要定义。默认为1行
- Ctrl+F 向下滚动一屏
- 空格键 向下滚动一屏
- Ctrl+B 返回上一屏
- = 输出当前行的行号
- ：f 输出文件名和当前行的行号
- V 调用vi编辑器
- !命令 调用Shell，并执行命令
- q 退出more

### less 命令
less 与 more 类似，less 可以随意浏览文件，支持翻页和搜索，支持向上翻页和向下翻页。

语法:
> less [参数] 文件 

参数：
- -b <缓冲区大小> 设置缓冲区的大小
- -e 当文件显示结束后，自动离开
- -f 强迫打开特殊文件，例如外围设备代号、目录和二进制文件
- -g 只标志最后搜索的关键词
- -i 忽略搜索时的大小写
- -m 显示类似more命令的百分比
- -N 显示每行的行号
- -o <文件名> 将less 输出的内容在指定文件中保存起来
- -Q 不使用警告音
- -s 显示连续空行为一行
- -S 行过长时间将超出部分舍弃
- -x <数字> 将"tab"键显示为规定的数字空格
- /字符串：向下搜索"字符串"的功能
- ?字符串：向上搜索"字符串"的功能
- n：重复前一个搜索（与 / 或 ? 有关）
- N：反向重复前一个搜索（与 / 或 ? 有关）
- b 向上翻一页
- d 向后翻半页
- h 显示帮助界面
- Q 退出less 命令
- u 向前滚动半页
- y 向前滚动一行
- 空格键 滚动一页
- 回车键 滚动一行
- [pagedown]： 向下翻动一页
- [pageup]： 向上翻动一页

实例:
```sh
# 查看文件
less log2013.log

# ps查看进程信息并通过less分页显示
ps -ef |less

# 查看命令历史使用记录并通过less分页显示
history | less

# 浏览多个文件
less log2013.log log2014.log
```

快捷键
- ctrl + F - 向前移动一屏
- ctrl + B - 向后移动一屏
- ctrl + D - 向前移动半屏
- ctrl + U - 向后移动半屏
- j - 下一行
- k - 上一行
- G - 移动到最后一行
- g - 移动到第一行
- q / ZZ - 退出 less 命令
- v - 使用配置的编辑器编辑当前文件
- h - 显示 less 的帮助文档
- &pattern - 仅显示匹配模式的行，而不是整个文件

### head 命令

### tail 命令

### which 命令

### whereis 命令

### locate 命令

### find 命令

### chmod 命令

### chown 命令

### df 命令

### du 命令

### ln 命令

### date 命令

### cal 命令

### grep 命令

### wc 命令

### ps 命令

### kill 命令

### free 命令
