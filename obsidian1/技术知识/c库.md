### strncat

```c
char *strncat(char *dest, const char *src, size_t n)
```

### strncpy

```c
char *strncpy(char *dest, const char *src, size_t n)
```

- 把 **src** 所指向的字符串复制到 **dest**，最多复制 **n** 个字符。当 src 的长度小于 n 时，dest 的剩余部分将用空字节填充。
- strncpy 没有自动加上终止符的。

### snprintf

```c
int snprintf ( char * str, size_t size, const char * format, ... );
```

- snprintf() 函数的返回值是输出到 str 缓冲区中的字符数，不包括字符串结尾的空字符 \0。
- 如果 snprintf() 输出的字符数超过了 size 参数指定的缓冲区大小，则输出的结果会被截断，只有 size - 1 个字符被写入缓冲区，最后一个字符为字符串结尾的空字符 \0。
---

exit是一个**库函数**，在进程正常结束时调用。

功能：关闭所有文件，终止正在执行的进程。

```c
#include <stdlib.h>
#define EXIT_FAILURE 1
#define EXIT_SUCCESS 0
void exit(int status);
```

_exit是一个**系统调用**，用来终止一个进程。

#include <unistd.h>

void _exit(int status);

exit与_exit都是用来正常退出进程，二者区别在于：

- exit库函数会先检查进程打开文件的状况，并且负责把文件缓冲区中的内容写回到文件中；
- 而_exit系统调用则不会，所以调用\_exit系统调用退出进程有可能会造成文件内容丢失。
- ---

[fopen、open、popen_51CTO博客_python subprocess popen](https://blog.51cto.com/ljy789/1764787)

open所需头文件：

- #include <sys/types.h>
    
- #include <sys/stat.h>
    
- #include <fcntl.h>
    

[fopen 参数mode - 肯定；爱 - 博客园 (cnblogs.com)](https://www.cnblogs.com/ai616818/archive/2012/04/26/2470918.html)

fopen函数的模式字符串可以用6个字符组成 r(read) 读 w(write) 写 a(append) 追加 t(text) 文本模式 b(banary) 二进制模式 + 读取和写入
FILE *fopen(const char *file_name, const char *mode);

文件使用方式由r、w、a、b、、+等6个字符拼成，其各字符的含义是：

r（read）读；

w（write）写；

a（append）添加；

b（binary）二进制文件；

t（text）文本文件，可省略；

\+ 读和写

*fopen ()*没有设定创建文件权限的参数，通过*fopen*创建的文件的权限是通过*0666 &*（*~umask*）得到的。



<io.h>

int open(char *path, int access, [, int auth]);



int select(int nfds, fd_set *readfds, fd_set *writefds, fd_set *exceptfds, struct timeval *timeout);

---
[linux timezone - dantes博客 - 博客园 (cnblogs.com)](https://www.cnblogs.com/dantes91/p/4670981.html)

[C/C++中的日期和时间 time_t与struct tm转换 - 吴文力 - 博客园 (cnblogs.com)](https://www.cnblogs.com/wiseman/archive/2005/10/24/260576.html)