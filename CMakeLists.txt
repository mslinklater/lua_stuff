cmake_minimum_required(VERSION 3.10)

set(CMAKE_C_FLAGS "-DDEBUG -DLUA_USE_POSIX")
set(CMAKE_BUILD_TYPE Debug)

project(lua_stuff LANGUAGES C)

add_subdirectory("lua-5.4.4/src")

add_executable(simple_interpreter simple_interpreter.c ${LUASOURCE_FILES})
target_link_libraries(simple_interpreter m)
