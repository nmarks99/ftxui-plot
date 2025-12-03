cmake_minimum_required (VERSION 3.22)

project(ftxui-plot)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 20)
# set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

include(cmake/ftxui.cmake)

add_library(ftxui-plot STATIC
    include/ftxui-plot/plot.hpp
    src/ftxui-plot/plot.cpp
)
target_link_libraries(ftxui-plot PUBLIC ftxui::component)

target_include_directories(ftxui-plot PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)

add_subdirectory(example)

# find_package(ftxui REQUIRED)
#
# add_executable(example src/main.cpp src/plot.cpp)
# target_include_directories(example PRIVATE src)
#
# target_link_libraries(example
  # PRIVATE ftxui::screen
  # PRIVATE ftxui::dom
  # PRIVATE ftxui::component
# )
