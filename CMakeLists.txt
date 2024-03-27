cmake_minimum_required(VERSION 3.20)

if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Debug)
endif()

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

project(miniserver LANGUAGES CXX)



file(GLOB_RECURSE SOURCES "code/*.cpp" "code/*.h")

add_executable(miniserver ${SOURCES})
target_link_libraries(miniserver PUBLIC mysqlclient)


