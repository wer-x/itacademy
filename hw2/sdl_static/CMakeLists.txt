cmake_minimum_required(VERSION 3.16)
project(02-sdl-static)

add_executable(02-sdl-static main.cxx)
target_compile_features(02-sdl-static PUBLIC cxx_std_17)

find_package(SDL2 REQUIRED)

target_link_libraries(02-sdl-static PRIVATE SDL2::SDL2-static)

install(TARGETS 02-sdl-static
        RUNTIME DESTINATION ${CMAKE_CURRENT_LIST_DIR}/../tests/hw2/bin
        LIBRARY DESTINATION ${CMAKE_CURRENT_LIST_DIR}/../tests/hw2/lib
        ARCHIVE DESTINATION ${CMAKE_CURRENT_LIST_DIR}/../tests/hw2/lib)
