# Example1 单个源文件

main.c

```c
#include <stdio.h>
int main(void)
{
    printf("HelloWorld\n");
    return 0;
}
```

CMakeLists.txt

```cmake
cmake_minimum_required (VERSION 2.8.12)
project(hello)
add_executable(hello main.c)
```

执行编译

```bash
mkdir build
cd build
cmake ..
make
```
