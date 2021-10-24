cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 14)

project(MyLab)

add_library(Calculator
	src/Calculator.h
	src/Calculator.cpp
)


target_include_directories(
	Calculator
	PUBLIC
		"src"
)

add_executable(start
  src/main.cpp
)

target_link_libraries(start Calculator)