cmake_minimum_required(VERSION 3.5.0)

set(CMAKE_EXPORT_COMPILE_COMMANDS True)
#set(CMAKE_BUILD_TYPE "Debug")

project(ysutil VERSION 0.1 LANGUAGES CXX)

message(DEBUG "PROJECT_SOURCE_DIR is ${PROJECT_SOURCE_DIR}")
message(DEBUG "PROJECT_BINARY_DIR is ${PROJECT_BINARY_DIR}")
message(DEBUG "CWD is ${CMAKE_CURRENT_SOURCE_DIR}")
message(DEBUG "current file is ${CMAKE_CURRENT_LIST_FILE}")

#把当前目录(.)下所有源代码文件和头文件加入变量DIR_SRCS
aux_source_directory(./include DIR_SRCS)
aux_source_directory(./src DIR_SRCS)

add_executable(ystest ${DIR_SRCS})