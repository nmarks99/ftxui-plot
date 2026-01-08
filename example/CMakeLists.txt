add_executable(ftxui-plot-example-static static.cpp)
target_link_libraries(ftxui-plot-example-static PRIVATE ftxui-plot)

add_executable(ftxui-plot-example-stream stream.cpp)
target_link_libraries(ftxui-plot-example-stream PRIVATE ftxui-plot)
