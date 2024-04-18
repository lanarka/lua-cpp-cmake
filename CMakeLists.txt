cmake_minimum_required(VERSION 3.12)
project (LuaCpp)
set(CMAKE_CXX_STANDARD 20)

file (GLOB LUA_SRC "Lua/include/*.h" "Lua/src/*.c")

include_directories("Lua/include")

add_executable(main 
	${LUA_SRC}
	src/main.cpp
)

target_link_libraries(main)
