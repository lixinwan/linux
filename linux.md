**linux学习1**

1.用户和用户组

UID；拥护的标识    管理员：0  系统用户：1-999   普通用户 ：1000-

GID：群组的标识：

三个主要文件：

/etc/passwd   UID

/etc/shadow   密码

/etc/group  GID

lixin:x:1000:1000:lixin,,,:/home/lixin:/bin/bash

su 用户名：切换用户

2.文件权限

用户权限  用户组权限 其他用户权限

r：读      w：写    x：执行

-rw-r--r--   :第一个-表示普通文件

<img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-11-10-16-23-image.png" title="" alt="" width="371">

修改文件权限

    sudo chmod 777 filename

    其中 777  111 111 111

liunx学习2

1.shell

用户与内核沟通桥梁 

shell与图像化界面： 

    图形化界面：鼠标操作为主，简单易学

    shell：键盘操作为主，需要记忆各种控制命令

shell命令：

    tab：自动补全

    man：查询命令

    --help

    cd / ：进入根目录

    cd~ ：返回目录终端

    cd .. :返回上一级

    pwd：打印当前目录路径

    ls：当前目录所有内容

    mkdir：创建文件夹

    redir：删除指定空目录

    mv：文件重命名 移动文件夹

    touch：创建文件

    cat：展示文件内容

    echo：写入数据并控制台输出

    rm：移除文件

    rm -rf  filename： 删除文件夹

    cp：复制

    tar：打包  解包

    grep：查找文本中字符串

    chomd：修改文件权限 -rwxrwxrwx  777     使用方法：sudo    chmod    777   文件

    ping：检查网络是否通

    ifconfig:网卡网络信息

    clear：清屏

    reboot：重启

    poweroff：关机

    ！！：重复命令 

    ls：查看目录下文件情况

    ls  -l  目录：查看目录下文件情况以及文件的详细情况

3.编译器

gedit：图形化界面，操作简单

vim：一般模式    插入模式     命令行模式

一般模式不能修改任何内容，只有切换到插入模式才行

<img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-11-14-46-54-image.png" title="" alt="" width="211">

vim  文件名

插入模式

    i：在当前光标所在位置插入文本    

    a：在当前光标所在位置的下一个字符插入文本

    o：在当前光标所在位置后插入新行

    r：替换当前光标所在位置的字符

    ESC：退出插入模式

普通模式常用命令：
    /word：在文件中搜索关键字word

    n：查找下一个关键字

    N：查找上一个关键字

    pageUp：向上翻页

    pageDown：向下翻页

    u：撤销上一步操作

    dw：删除一个单词

    dd；删除一行

    yy：复制一行内容

    y：复制光标所选字符

    p：将复制的数据粘贴在当前行的下一行

    v：选择多个字符

    V：可以选择多行 

命令行模式：

    w:保存文档

    w <filename>：另存为名为<filename>的文档

    q：直接退出软件，前提是文档未做任何修改

    q！：不保存修改，直接退出软件

    qw：保存文档，并退出    

    set nu：加入行号

    set nonu：不加入行号

主要命令 i    Esc    ：    x    wq    q！ 

########虚拟机网络设置#################

网络：sudo service network-manager stop

sudo rm /var/lib/NetworkManager/NetworkManager.state

sudo service network-manager start
