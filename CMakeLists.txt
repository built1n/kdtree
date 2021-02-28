cmake_minimum_required(VERSION 3.0)

project(kdtree)

set(CMAKE_C_STANDARD 99)

add_library(kdtree SHARED kdtree.c kdtree.h)

set_target_properties(kdtree PROPERTIES PUBLIC_HEADER kdtree.h)

install(TARGETS kdtree
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
