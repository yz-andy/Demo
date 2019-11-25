1. sudo apt-get install "软件名称"

   在Linux 系统终端里面输入：次命令，即可下载

2. sudo apt-get update 

   软件更新指令 在其资源网站里找到最新的软件资源

3. pwd 查看目录

4. ls 查看家 目录

5. ls -l 查看目录文件所建立修改的时间

6. r: 可读    w: 可写  x:可执行

7. #include <stdio.h> // 导入标准输入输出库的头文件

8. n (函数的行数) + dd

   剪贴某函数

9. 

10.  ：sp ＋ 文件名称  在终端窗口同时显示两个窗口

11.  ：Ctrl + W + 方向键 上，下 尽可切换不同窗口 

12.  : ：wqa   所有的文件都保存都退出

13. ：cc max.c hello.c -o "main.out(输出程序的名称)"  输出一个文件

14. ls -l 查看文件属性

15. cp max.c 拷贝 复制 内容到新文件（min.c 新文件名称）

16. cc max.o hello.c 生成一个a.out 输出文件

17.  ./a.out 输出

18. 不会在修改的函数，公共框架，公共类  优先生成一个静态库

19. 

20. 检查是否安装make 软件  make -v

     删除所有项目文件后面  " .o "的文件  ,查看项目文件

    vim Makefile 创建并打开Makefile 文件

    文件Makefile里面所有的内容:

    (#this is make file[注释]

    hello.out:max.o min.o hello.c

    ​				gcc max.o min.o hello.c 指令

    max.o:max.c

    ​				gcc -c max.c       指令

    min.o:min.c

    ​				gcc - min.c      指令

    )  

    退出保存：wq

21. suto apt-get install make 安装make

22. %s 打印一个字符串

23. scanf 输入指令

24. 指针：指向资源的指针

25. stdin： 标准输入流      ------>   键盘输入

26. stdout ：标准输出流  --------> 终端输出

27. stderr ：标准错误流 -------->错误输出

28. ./a.out >> a.txt  重定向（追加模式，依次累加）

29. ./a.out > a.txt   重定向（刷新模式显示最近更新的内容）

30. scanf("%d",&i);  每一次的接受的输入 那输入的结果放入&i

31. ps -e 查询进程文件的命令  程序的进程

32. pe -e | grep "字符串"

33. 

    

