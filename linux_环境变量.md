**linux学习3**

1.linux环境变量

全局变量：用前面shell语言直接定义，但定义的变量不能被shell其他进程或子进程访问

export：可以被shell子进程访问，但不能被其他进程访问

Bash Shell有关的配置文件主要有

    1./etc/profile  所用用户第一次登录时才执行

    2.~/.bash_profile

    3.~/.bash_login

    4.~/.profile  当前用户第一次登录时才执行

    5.~/.bashrc  一个用户、全部进程共享

    6./etc/bashrc

    7./etc/bash.bashrc  全部用户、全部进程共享

    8./etc/profile.d/*.sh

shell执行顺序

     /etc/profile->~/.profile

    其中还78在1中调用，5在4中调用

shell启动方式对变量的影响

    子shell进程中执行/bin/bash和/

    当前进程中执行source和.

    
