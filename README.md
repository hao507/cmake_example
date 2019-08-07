# CMake笔记

## 基本语法

| 定义      | 语法
| :---      | ---
| 版本      | `cmake_minimum_required (VERSION 2.8.12)`
| 项目名称  | `project (name)`
| 变量      | `set (VARIABLE 1)` `set(VARIABLE a b c)`
| 变量引用  | `${VARIALBE}`
| 条件判断  | `if ()` `else()` `endif()`
| 循环      | `foreach (p ${VAR})`
| 输出消息  | `message()`
| 生成库    | `add_library(name ATTR ${src})`
| 生成可执行文件 | `add_executable(name ${src})`

## 常用参数

| 参数      | 说明
| :---      | ---
| -G        | 指定生成哪种工程，如`-G"NMake Makefiles"`

## 示例

- [Example1: 单个源文件](example1/README.md)
- [Example2: 多个源文件](example2/README.md)
