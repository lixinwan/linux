**GCC**

1.GCC由来

    GUN组织    unix系统    minix系统    posix接口     internet

2.GCC编译工具链

    gcc编译器（预处理、编译）

    binutils工具集（汇编、链接）

3.gcc编译

    sudo gcc hello.c   -o    hello       不加-o默认编译成a.out    

    文件.s    都是汇编文件

4.其它系统安装gcc

    sudo apt install gcc -y     -y:表示默认选项，不需要额外咨询我

    which gcc 查看GCC安装位置

5.三个问题

   （1） ARM-GCC是什么？它与GCC有什么关系？

            编译工具链和目标程序运行相同的架构平台，就叫本地编译

            编译工具链和目标程序运行在不同的架构平台，就叫交叉编译

            ARM-GCC是针对arm平台的一款编译器，它是GCC编译工具链的分支

   （2）ARM-GCC进一步分类有哪些？

            ![](C:\Users\li'xin\AppData\Roaming\marktext\images\2022-08-15-20-32-24-image.png)

            ![](C:\Users\li'xin\AppData\Roaming\marktext\images\2022-08-15-20-36-46-image.png)

            第二项：linux    none

            第三项：gnu：glibc    eabi：应用二进制标准接口      hf：支持硬浮点平台

   （3） 如何安装ARM-GCC？

            apt  install gcc  

            apt install gcc-arm-linux-gnueabihf   安装arm版本GCC

Linaro公司

6.两个案列

    在ARM架构上运行x86_64架构的程序    不可行，编译格式不一样

    在ARM架构上运行交叉编译的程序       可行

**linux系统和Helloword**

1.三个问题

    （1）了解Hello World程序的执行过程有什么用？

            1.对开发其他应用程序，有非常好的借鉴意义。

            2.对程序的报错有清晰的了解，从而针对性的解决问题。 

    （2）逻辑开发中的Helloworld程序是怎么执行的？

    （3）Linux系统下的Hello    World程序是怎么执行的？   

2.裸机开发中的Hello  World程序是怎么执行的？

<img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-15-21-31-18-image.png" title="" alt="" width="483">

3.Linux系统下的Hello world程序是怎么执行的？

    
