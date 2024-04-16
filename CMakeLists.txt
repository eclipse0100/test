cmake_minimum_required(VERSION 3.10.0)

set(CMAKE_TOOLCHAIN_FILE "C:/git/vcpkg/scripts/buildsystems/vcpkg.cmake" CACHE FILEPATH "Path to toolchain")

project(ansicolor VERSION 0.1.0 LANGUAGES C CXX)

# include(CTest)
# enable_testing()

find_path(TERMCOLOR_INCLUDE_DIRS "termcolor/termcolor.hpp")

add_executable(ansicolor main.cpp)

target_include_directories(ansicolor PRIVATE ${TERMCOLOR_INCLUDE_DIRS})

# set(CPACK_PROJECT_NAME ${PROJECT_NAME})
# set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
# include(CPack)
