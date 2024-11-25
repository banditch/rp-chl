cmake_minimum_required(VERSION 3.10)
project(LightweightBrowser)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK REQUIRED gtk+-3.0 webkit2gtk-4.0)

include_directories(${GTK_INCLUDE_DIRS})
link_directories(${GTK_LIBRARY_DIRS})

add_executable(lightbrowser src/main.cpp)
target_link_libraries(lightbrowser ${GTK_LIBRARIES})
