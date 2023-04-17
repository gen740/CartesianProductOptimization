cmake_minimum_required(VERSION 3.20)

project(CartesianProduct C)


add_executable(CartesianProduct src/main.c)

find_package(benchmark CONFIG REQUIRED)

target_link_libraries(CartesianProduct benchmark::benchmark)
target_include_directories(CartesianProduct PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)
target_compile_options(CartesianProduct PRIVATE -O3 -Wall)
