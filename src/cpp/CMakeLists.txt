cmake_minimum_required(VERSION 3.19)
set(CMAKE_CXX_STANDARD 17)
project(BPLM)


# MSVC utf-8
add_compile_options("$<$<C_COMPILER_ID:MSVC>:/source-charset:utf-8>")
add_compile_options("$<$<CXX_COMPILER_ID:MSVC>:/source-charset:utf-8>")


# GNU utf-8
add_compile_options("$<$<C_COMPILER_ID:GNU>:-fexec-charset=GBK>")
add_compile_options("$<$<CXX_COMPILER_ID:GNU>:-fexec-charset=GBK>")
add_compile_options("$<$<C_COMPILER_ID:GNU>:-finput-charset=utf-8>")
add_compile_options("$<$<CXX_COMPILER_ID:GNU>:-finput-charset=utf-8>")


file(GLOB SRCS
	"./*"
)

add_executable(BPLM ${SRCS})
