cmake_minimum_required (VERSION 3.10)
project(example-imtui)

set(CMAKE_EXPORT_COMPILE_COMMANDS "on")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

add_subdirectory(third-party)

find_package(PkgConfig REQUIRED)
pkg_check_modules(LIBBITCOIN_SYSTEM REQUIRED IMPORTED_TARGET libbitcoin)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(src)

