# Example3: 生成库并链接库

我们把hello.c生成库libhello.a，然后生成hello可执行程序。生成库需要用到`add_library()`，用法同`add_executable()`相同，需要指定生成库的名称和关联的源文件。需要注意的是，库作为target的一种，不能和同为target的可执行程序同名。如果可执行程序名为hello，那么库就不能叫做hello。而如果将库的名字改为libhello，实际生成的库名字将为liblibhello，前缀lib是自动生成的。可以通过`set_target_properties(libhello PROPERTIES OUTPUT_NAME "hello")`改变输出库的名称。 
  
文件结构

```
./
build/
CMakeLists.txt*
hello.c*
hello.h*
main.c*
```

CMakeLists.txt

```cmake
cmake_minimum_required (VERSION 2.8.12)
project(hello)
add_library(libhello hello.c)
add_executable(hello main.c)
target_link_libraries(hello libhello)
set_target_properties(libhello PROPERTIES OUTPUT_NAME "hello")
```

执行编译

```bash
mkdir build
cd build
cmake ..
make
```
