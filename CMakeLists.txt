project (BTech)
cmake_minimum_required (VERSION 2.8)
find_package (Qt5 COMPONENTS Core Gui Widgets)
set (CMAKE_CXX_FLAGS "-Wall -std=c++11 -ggdb -pg")

include_directories (${Qt5Widgets_INCLUDE_DIRS} ${BTech_SOURCE_DIR}/src)
set (EXECUTABLE_OUTPUT_PATH "${BTech_BINARY_DIR}/bin")
set (LIBRARY_OUTPUT_PATH "${BTech_BINARY_DIR}/lib")

add_subdirectory (src)

install (DIRECTORY data DESTINATION "${BTech_BINARY_DIR}")
