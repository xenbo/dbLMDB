cmake_minimum_required(VERSION 3.8)
project(dbLMDB)

add_definitions(-g)

set(CMAKE_C_STANDARD 99)

set(SOURCE_FILES midl.c midl.h mdb.c lmdb.h)
add_library(dblmdb ${SOURCE_FILES})

set(SOURCE_FILES2 main.c)
add_executable(dbLMDB ${SOURCE_FILES2})
target_link_libraries(dbLMDB dblmdb pthread)