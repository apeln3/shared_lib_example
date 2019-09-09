cmake_minimum_required(VERSION 2.8)
project(tester)



set(LIB_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/print_lib)

add_subdirectory(print_lib)

include_directories(${LIB_INCLUDE_DIR})


add_executable(tester main.cpp)

target_link_libraries(tester print_lib)
ADD_DEPENDENCIES(tester print_lib)
