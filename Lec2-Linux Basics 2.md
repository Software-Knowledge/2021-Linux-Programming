Lec2-Linux Basics 2
---

# 1. 基本命令(1)
1. 文件操作
   1. 列出目录内容: ls, dir, vdir
   2. 创建特殊文件: mkdir, mknod, mkfifo
   3. 文件操作: cp, mv, rm
   4. 修改文件属性: chmod, chown, chgrp, touch
   5. 查找文件: locate, find
   6. 字符串匹配: grep(egrep)
   7. 其它: pwd, cd, ar, file, tar, more, less, head, tail, cat
2. 进程操作：ps, kill, jobs, fg, bg, nice
3. 其它
   1. who, whoami, passwd, su, uname, …
   2. man

# 2. 重定向
1. 标准输入、标准输出、标准错误
   1. 对应的文件描述符：0, 1, 2
   2. C语言变量：stdin, stdout, stderr
2. <, >, >>, 2>
   1. 例：kill –HUP 1234 > killout.txt 2> killerr.txt
   2. 例：kill –HUP 1234 > killout.txt 2>& 1

# 3. 管道
1. 一个进程的输出作为另一个进程的输入
2. 例:
   1. ls | wc –l
   2. ls –lF | grep ^d
   3. ar t /usr/lib/libc.a | grep printf | pr -4 -t

# 4. 环境变量
1. 环境变量
   1. 操作环境的参数
   2. 查看和设置环境变量：echo, env, set
2. 例: PATH环境变量
   1. echo $PATH
   2. /usr/local/bin:/bin:/usr/bin:/usr/X11R6/bin:/home/song/bin
   3. PATH=$PATH:.
   4. export PATH

# 5. 高级命令与正则表达式
1. find
2. sed：sed 's/\([0-9A-Za-z_]\{1,\}\)\[ \{0,\}\]\[ \{0,\}\]/*\1\[\]/g' code1.cpp
3. grep