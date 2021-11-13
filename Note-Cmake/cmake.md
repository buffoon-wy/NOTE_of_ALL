# cmake  note
---
 
##2021.11.12
reference link :[cmake 入门实战]（https://www.hahack.com/codes/cmake/）
		[camke 命令介绍]（https://www.jianshu.com/p/e7de3de1b0fa）
GitHub：[git](https://github.com/wzpan/cmake-demo)

*流程*
使用cmake命令根据CMakeLists.txt文件生成make file，再使用make命令根据makefile文件进行编译

*注意*
- 'add_subdirectory(math)'
添加一个子目录并构建该子目录。
- 'include_directories ("${PROJECT_SOURCE_DIR}/math") '
将指定目录添加到编译器的头文件搜索路径之下，指定的目录被解释成当前源码路径的相对路径。
- 'message("the project source dir is = ${PROJECT_SOURCE_DIR}")'
可将变量的值打印到终端



