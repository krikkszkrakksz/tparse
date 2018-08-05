cmake_minimum_required(VERSION 3.10)
project(torrents)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

include_directories(libs)

set(CMAKE_AUTOMOC_MOC_OPTIONS -p ${CMAKE_SOURCE_DIR}/src)
find_package(Qt5Widgets CONFIG REQUIRED)

add_executable(torrents src/main.cpp)
target_link_libraries(torrents Qt5::Widgets)
