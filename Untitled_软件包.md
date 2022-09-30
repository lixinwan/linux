**linux学习3**

Linux软件包

1.软件包组成：

   文件类型    保存目录

    普通程序    /usr/bin

    root权限程序    /usr/sbin

    程序配置文件    /etc

    日志文件           /var/log

    文档文件    /usr/share/doc

2.linux软件包

    源码包：开源免费、自由裁剪、修改源代码、安装麻烦、编译时间长

    软件包：简单易用、安装速度快、无法修改源代码、无裁剪功能，依赖性强

3.包分类

    ded包：Debian、ubuntu、Deepin发行的安装包

    rpm包：RedHat、Fedora、Centos发行的包

4.dpkg工具

    安装软件：dpkg -i xxxx.deb

    卸载软件：dpkg -r xxxx

    查看安装目录：dpkg  -L    xxxx

    显示版本信息：dpkg    -l    xxxx

5.deb包文件结构分析

    control文件

    postinst文件：安装之后执行的shell脚本

6.构建一个helloworld的deb包

    演示：dpkg -b

    其他：

    dpkg-buildpackage

    checkinstall

7.apt命令和apt-get命令

    apt是新版的包管理工具

    解决apt-get命令过于分散的问题

    apt默认属性对用户友好（进度条、提示升级包数）

    安装包

    1.刷新软件包    sudo apt update       原来  sudo apt-get  update

    2.安装包    sudo apt  install   xxx
