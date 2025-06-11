cmake_minimum_required(VERSION 3.10.0)
project(material-color-utilities-cpp VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

file(GLOB_RECURSE SOURCES
    "src/*.cpp"
    "src/*.cc"
)
add_library(material-color-utilities-cpp ${SOURCES})
target_include_directories(material-color-utilities-cpp PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/src>
    $<INSTALL_INTERFACE:include>
)
