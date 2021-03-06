# Linux（二）
[TOC]

* * *

## Linux 文件基本属性
在Linux中我们可以使用ll或者ls –l命令来显示一个文件的属性以及文件所属的用户和组，如

> [root@www /]# ls -l
> total 64
> dr-xr-xr-x   2 root root 4096 Dec 14  2012 bin
> dr-xr-xr-x   4 root root 4096 Apr 19  2012 boot
> ……

实例中，bin文件的第一个属性用"d"表示。"d"在Linux中代表该文件是一个目录文件。
在Linux中第一个字符代表这个文件是目录、文件或链接文件等等。

当为[ d ]则是目录
当为[ - ]则是文件；
若是[ l ]则表示为链接文档(link file)；
若是[ b ]则表示为装置文件里面的可供储存的接口设备(可随机存取装置)；
若是[ c ]则表示为装置文件里面的串行端口设备，例如键盘、鼠标(一次性读取装置)。

接下来的字符中，以三个为一组，且均为『rwx』 的三个参数的组合。其中，[ r ]代表可读(read)、[ w ]代表可写(write)、[ x ]代表可执行(execute)。 要注意的是，这三个权限的位置不会改变，如果没有权限，就会出现减号[ - ]而已。
每个文件的属性由左边第一部分的10个字符来确定（如下图）。
![](http://www.runoob.com/wp-content/uploads/2014/06/363003_1227493859FdXT.png)
从左至右用0-9这些数字来表示。
第0位确定文件类型，第1-3位确定属主（该文件的所有者）拥有该文件的权限。
第4-6位确定属组（所有者的同组用户）拥有该文件的权限，第7-9位确定其他用户拥有该文件的权限。
其中，第1、4、7位表示读权限，如果用"r"字符表示，则有读权限，如果用"-"字符表示，则没有读权限；
第2、5、8位表示写权限，如果用"w"字符表示，则有写权限，如果用"-"字符表示没有写权限；第3、6、9位表示可执行权限，如果用"x"字符表示，则有执行权限，如果用"-"字符表示，则没有执行权限。