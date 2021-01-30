gcc -c Hello.c 会先产生Hello.o目标文件，，不是直接编译为可执行的二进制文件
-rw-r--r--    1 root     root            73 Jan 30 03:16 Hello.c
-rw-r--r--    1 root     root          1536 Jan 30 03:16 Hello.o

gcc -o hello Hello.o 会产生可执行文件hello
drwxr-xr-x    2 root     root            67 Jan 30 03:20 .
drwxr-xr-x    5 root     root            57 Jan 30 03:11 ..
-rw-r--r--    1 root     root            73 Jan 30 03:16 Hello.c
-rw-r--r--    1 root     root          1536 Jan 30 03:16 Hello.o
-rw-r--r--    1 root     root           231 Jan 30 03:19 README.txt
-rwxr-xr-x    1 root     root         19880 Jan 30 03:20 hello

./hello 执行程序运行结果
Hello World
!

gcc -c hello.c thank.c 联合编译产生两个目标文件
drwxr-xr-x    2 root     root           127 Jan 30 03:32 .
drwxr-xr-x    5 root     root            57 Jan 30 03:11 ..
-rw-r--r--    1 root     root            73 Jan 30 03:16 Hello.c
-rw-r--r--    1 root     root          1536 Jan 30 03:16 Hello.o
-rw-r--r--    1 root     root           711 Jan 30 03:26 README.txt
-rwxr-xr-x    1 root     root         19880 Jan 30 03:20 hello
-rw-r--r--    1 root     root            86 Jan 30 03:29 hello.c
-rw-r--r--    1 root     root          1592 Jan 30 03:32 hello.o
-rw-r--r--    1 root     root            62 Jan 30 03:31 thank.c
-rw-r--r--    1 root     root          1528 Jan 30 03:32 thank.o


gcc -o thank hello.o thank.o 两个目标文件一起产生可执行文件thank
drwxr-xr-x    2 root     root           141 Jan 30 03:34 .
drwxr-xr-x    5 root     root            57 Jan 30 03:11 ..
-rw-r--r--    1 root     root            73 Jan 30 03:16 Hello.c
-rw-r--r--    1 root     root          1536 Jan 30 03:16 Hello.o
-rw-r--r--    1 root     root          1360 Jan 30 03:33 README.txt
-rwxr-xr-x    1 root     root         19880 Jan 30 03:20 hello
-rw-r--r--    1 root     root            86 Jan 30 03:29 hello.c
-rw-r--r--    1 root     root          1592 Jan 30 03:32 hello.o
-rw-r--r--    1 root     root            62 Jan 30 03:31 thank.c
-rw-r--r--    1 root     root          1528 Jan 30 03:32 thank.o
-rwxr-xr-x    1 root     root         19936 Jan 30 03:34 thanks


gcc hello3.c -o hello3 -include thank3.h thank3.c 联合自己编写的头文件进行编译
-rwxr-xr-x    1 root     root         19944 Jan 30 03:59 hello3
-rw-r--r--    1 root     root           105 Jan 30 03:41 hello3.c
-rw-r--r--    1 root     root            66 Jan 30 03:47 thank3.c
-rw-r--r--    1 root     root            74 Jan 30 03:59 thank3.h

其他参数：
-l:是加入某个函数库的意思；
如-lm:表示加入libm.so这个函数库，lib与扩展名(.a\.so)不需要写
后面需要-L/path表明函数库位置
-I/path 表示（自定义、标准）头文件的位置
