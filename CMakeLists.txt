cmake_minimum_required (VERSION 2.8)

project (Bar)

set (FOOCompileTools_DIR ${CMAKE_CURRENT_SOURCE_DIR})
find_package (FOOCompileTools NO_MODULE REQUIRED)

add_custom_command(
      OUTPUT ${CMAKE_CURRENT_BINARY_DIR}/main.cxx
      DEPENDS main.cxx.in fooConfigureMain
      COMMAND fooConfigureMain
      ARGS ${CMAKE_CURRENT_SOURCE_DIR}/configure.py ${CMAKE_CURRENT_SOURCE_DIR}/main.cxx.in ${CMAKE_CURRENT_BINARY_DIR}/main.cxx
      )

add_executable (foo WIN32 ${CMAKE_CURRENT_BINARY_DIR}/main.cxx)
