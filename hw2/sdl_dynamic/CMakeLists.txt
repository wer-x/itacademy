cmake_minimum_required(VERSION 3.16)
project(02-sdl-dynamic)

add_executable(02-sdl-dynamic main.cxx)
target_compile_features(02-sdl-dynamic PUBLIC cxx_std_17)

find_library(SDL2_LIB_dyn libSDL2-2.0.so.0)

target_link_libraries(02-sdl-dynamic ${SDL2_LIB_dyn})

install(TARGETS 02-sdl-dynamic
        RUNTIME DESTINATION ${CMAKE_CURRENT_LIST_DIR}/../tests/hw2/bin
        LIBRARY DESTINATION ${CMAKE_CURRENT_LIST_DIR}/../tests/hw2/lib
        ARCHIVE DESTINATION ${CMAKE_CURRENT_LIST_DIR}/../tests/hw2/lib)

