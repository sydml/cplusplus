cmake_minimum_required(VERSION 3.19)
project(cplusplus)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(leetcode)

#链接库
aux_source_directory(leetcode/editor/cn/ LEETCODE)
add_library(leetcode ${LEETCODE})
LINK_LIBRARIES(leetcode)

add_executable(cplusplus leetcode/editor/cn/shu-zu-zhong-zhong-fu-de-shu-zi-lcof.cpp)
add_executable(ti-huan-kong-ge-lcof leetcode/editor/cn/ti-huan-kong-ge-lcof.cpp)

add_executable(er-jin-zhi-zhong-1de-ge-shu-lcof leetcode/editor/cn/er-jin-zhi-zhong-1de-ge-shu-lcof.cpp)