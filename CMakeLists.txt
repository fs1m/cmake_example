cmake_minimum_required(VERSION 3.19.2)

set(CMAKE_TOOLCHAIN_FILE "vcpkg/scripts/buildsystems/vcpkg.cmake")

project(test)

file(GLOB_RECURSE fileCollection "src/*.cpp")

find_package(SDL2 CONFIG REQUIRED)
add_executable(test ${fileCollection})
target_link_libraries(test PRIVATE SDL2::SDL2 SDL2::SDL2main)