**Makefile**

1.Makefile是什么？

    之前编译：gcc    hello.c    -o    hello

    现在：

    make工具和Makefile

2.make和Makefile是什么关系？

    make工具：找出修改过的文件，根据依赖关系，找出受影响的相关文件，最后按照规则单独编译这些文件。

    Makefile文件：记录依赖关系和编译规则。

3.必须要学精Makefile吗？

4.怎么学习Makefile？

    Makefile的本质：无论多么复杂的语法，都是为了更好地解决项目文件之间的依赖关系

![](C:\Users\li'xin\AppData\Roaming\marktext\images\2022-08-16-10-03-53-image.png)5.Makefile三要素是什么？

    目标、依赖、命令

6.怎么描述三要素的关系？

    目标：依赖的文件或者是其他目标

    <tab>命令1

    <tab>命令2

    <tab>命令3

7.实验演示

    .PHONY可以指定一个伪目标

8.Makefile变量

    变量：

    系统变量

        <img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-16-10-46-29-image.png" title="" alt="" width="178">

    自定义变量

        =，延迟赋值            最后赋值才有效

        ：=，立即赋值           赋值立即生效

        ？=，空赋值    变量为空赋值才有效

        +=，追加赋值        不会覆盖原有的值，只会添加到原来值后面

    自动化变量

        $<：第一个依赖文件

        $^：全部的依赖文件

        $@：目标

        MP3：main.o   mp3.o

                    gcc    main.o    mp3.o    -o    mp3

        其中，main.o  mp3.o是依赖，MP3是目标

        <img title="" src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-16-10-57-04-image.png" alt="" width="529">

        变量运用的例子：

        <img title="" src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-16-10-59-06-image.png" alt="" width="196">

    sudo  make：自动寻找nakefile文件，如果需要编译其他Makefile文件，则使用

    sudo make  -f   makefile文件

9.模式匹配

    %：匹配任意多个非空字符

    shell：*通配符

    <img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-16-11-06-08-image.png" title="" alt="" width="501">

10.默认规则

    .o文件默认使用.c文件来进行编译

11.Makefile条件分支

    ifeq(var1,var2)    #判断是否相等

    ...

    else

    ...

    endif

    ifneq(var1,var2)      #判断是否不相等

    ...

    else

    ...

    endif

    ****注意事项****

    sudo  cp -r  part_3  part_4  将文件夹3复制到文件夹4中去

12.Makefile常用函数

    patsubst：模式替换函数

    <img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-16-14-14-26-image.png" title="" alt="" width="540">

    notdir：去文件名

    <img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-16-14-16-18-image.png" title="" alt="" width="542">

    wildcard：列出当前目录下所有符合模式“PATTERN”的文件名

    ![](C:\Users\li'xin\AppData\Roaming\marktext\images\2022-08-16-14-19-00-image.png)

    foreach：查找文件夹下的文件

    <img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-16-14-23-07-image.png" title="" alt="" width="541">

12.Makefile解决头文件依赖问题

    1.写一个头文件，并把头文件添加到编译器的头文件路径中。

          gcc -I + “头文件路径”

    2.实时检查头文件的更新情况，一旦头文件发生变化，应该要重新编译所有相关文件。
