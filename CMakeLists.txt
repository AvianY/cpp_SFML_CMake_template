cmake_minimum_required(VERSION 3.0.0)
project(cpp_SFML_CMake_template VERSION 0.1.0)

set(SFML_DIR "SFML-2.5.1/lib/cmake/SFML")
find_package(SFML 2.5.1 COMPONENTS graphics REQUIRED)

include_directories(
    "SFML-2.5.1/include/"
    "include/"
)

add_executable(main
    src/main.cc
)

target_link_libraries(main sfml-graphics)