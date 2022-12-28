project(embedding-test)
cmake_minimum_required(VERSION 3.24)

add_library(v8 STATIC IMPORTED)
set_property(TARGET v8 PROPERTY
             IMPORTED_LOCATION 
             "${CMAKE_SOURCE_DIR}/arm64.debug.mac/libv8_monolith.a")
target_include_directories(v8 INTERFACE 
    "${CMAKE_SOURCE_DIR}"
    "${CMAKE_SOURCE_DIR}/include"
)

add_executable(shell_test shell.cc)
target_link_libraries(shell_test PRIVATE v8)
add_compile_definitions(V8_COMPRESS_POINTERS)

set_property(TARGET shell_test PROPERTY CXX_STANDARD 17)
