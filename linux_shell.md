**linux学习2**

1.shell脚本编程

 shell脚本作用：软件启动    性能监控    日志分析

shell的本质：内置命令/外部命令

    输入命令，先去内置命令里面取查找

    再去PATH里面查找

shell脚本语言和C语言一样吗？

    编译型语言  c

    解释型语言  shell

第一个shell脚本

    lixin    hello！

    编辑、保存、改权限、运行/排错

常用shell解析器

    cat /etc/shells

shell启动方式

    当程序执行  ./hello.sh

    指定解释器运行    /bin/dash hello.sh

    source和.     source hello.sh        .  hello.sh

2.shell脚本语法讲解

定义变量

    variable=value  该定义方式变量不能有空格

    variable='value'    该定义方式变量允许有空格  不可以输出引用变量，原封不动打印字符

    variable="value"    该定义方式变量允许有空格   可以输出引用变量

使用变量

    $variable    自动识别后面变量，可能识别错误

    ${variable}    手动识别，做到边界确认，保证识别正确

将命令结果赋值给变量  

    variable=`command`

    variable=$(command)

删除变量

    unset

特殊变量

    $0：当前脚本的文件名

    $n：传递给脚本的参数

    $#：传递给脚本或函数的参数个数

    $* ：传递给脚本或函数的所有参数

    $？：上个命令的退出状态或获取函数返回值

    $$  ：当前shell进程的ID

字符串

    并排放

退出当前进程

    exit

对整数进行数学运算

    （()）

<img title="" src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-11-20-22-52-image.png" alt="" data-align="inline" width="198">

逻辑与/或

    command1 && command2 :先判断command1是否成立，成立执行command2

    command1 || command2：先判断command1是否不成立，不成立执行command2

检测某个条件是否成立

    test   expression 和 [expression]    

   -eq ：判断是否相等

    -ne：判断是否不相等

    -gt：判断数值是否大于

    -lt：判断数值是否小于

    -ge：判断是否大于等于

    -le：判断是否小于等于

    -z   str：判断字符串是否为空

    -n   str：判断字符串str是否非空

    =和==：判断字符串str是否相等

    -d  filename ：判断文件是否存在，并且是否未目录文件

    command1 | command2 ：command1输出信息作为command2输入信息，command1不能有错误

<img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-11-21-22-41-image.png" title="" alt="" width="288">

if语句

    if    condition

    then

                statement1

    fi

if else语句

    if    condition

    then

                statement1

    else

                 statement2

    fi

if elif else语句

    if    condition

    then

                statement1

    elif    condition2

    then

                  statement2

    else

                   statement3

    fi

<img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-11-21-38-53-image.png" title="" alt="" width="195">

case in 语句（与C语言中swich case一样）

    case expression   in

              pattern1)

                    statement1

                     ;;

               pattern2)    

                     statement2

                     ;;

                pattern3）

                       statement3

                        ;;

                  *)

                         statementn

      esac

<img src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-12-09-49-17-image.png" title="" alt="" width="251">

for in循环

    for    variable    in    value_list

    do

        statements

    done

    其中 value_list

        直接给出具体的值     1 2 3 4 5

        直接给出一个取值范围    {1..5}

        使用命令的执行结果    $(ls  /bin)

        使用shell通配符

        使用特殊变量    $@

<img title="" src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-12-10-04-42-image.png" alt="" width="250">

while 循环

    while condition

    do

        statements

    done        

<img title="" src="file:///C:/Users/li'xin/AppData/Roaming/marktext/images/2022-08-12-10-09-48-image.png" alt="" data-align="inline">

函数

    function name()

    {

        statements

        {return    value}

    }

![](C:\Users\li'xin\AppData\Roaming\marktext\images\2022-08-12-10-12-34-image.png)
