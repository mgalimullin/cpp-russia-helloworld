cmake_minimum_required(VERSION 2.8.7)

project(hello CXX)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

include_directories(include)

set(${PROJECT_NAME}_SRC
	src/hello.cpp
)

add_library(${PROJECT_NAME} ${${PROJECT_NAME}_SRC})


enable_testing()
add_subdirectory(test)