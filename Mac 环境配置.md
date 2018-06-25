# Mac 环境配置

### 下载源代码

在 http://www.apuebook.com 网站下载 apue 源代码

### 编译

在 apue.3e 目录下输入 make

```
cd apue.3e
make
```

### 把 apue 库放入系统库

```
cp ./include/apue.h /usr/local/include/
cp ./lib/error.c /usr/local/include/
```

修改 apue.h

```
vi /usr/local/include/apue.h
```

最后一行#end if之前插入

```
#include "error.c"
```

### 测试

在 apue.3e/intro 目录下

```
clang hello.c
./a.out
```



