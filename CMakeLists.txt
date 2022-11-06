cmake_minimum_required(VERSION 3.24)

set(CMAKE_TOOLCHAIN_FILE ${CMAKE_CURRENT_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake)

project("vcpkg_test" CXX)

find_package(fmt CONFIG REQUIRED)

add_executable(${PROJECT_NAME}
    main.cpp
)

target_link_libraries(${PROJECT_NAME} PRIVATE fmt::fmt)
