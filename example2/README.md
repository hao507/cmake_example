# Example2: 多个源文件

文件结构

```
./
build/
CMakeLists.txt*
hello.c*
hello.h*
main.c*
```

main.c

```c
#include "hello.h"

int main(void)
{
    hello();
    return 0;
}
```

hello.c

```c
#include <stdio.h>

void hello(void)
{
    printf("HelloWorld\n");
}
```

hello.h

```c
#ifndef HELLO_H_
#define HELLO_H_

extern void hello(void);

#endif
```

CMakeLists.txt

```cmake
cmake_minimum_required (VERSION 2.8.12)
project(hello)
add_executable(hello main.c hello.c)
```

执行编译

```bash
mkdir build
cd build
cmake ..
make
```
