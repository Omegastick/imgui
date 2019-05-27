cmake_minimum_required(VERSION 3.5.1)
project(DearIMGUI)

add_library(imgui STATIC)

target_include_directories(imgui 
PUBLIC 
    .
    examples
    ../GLFW/include
    ../GLAD/include
)

target_sources(imgui 
PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/imgui_demo.cpp
    ${CMAKE_CURRENT_LIST_DIR}/imgui_draw.cpp
    ${CMAKE_CURRENT_LIST_DIR}/imgui_widgets.cpp
    ${CMAKE_CURRENT_LIST_DIR}/imgui.cpp
    ${CMAKE_CURRENT_LIST_DIR}/examples/imgui_impl_glfw.cpp
    ${CMAKE_CURRENT_LIST_DIR}/examples/imgui_impl_opengl3.cpp
    ${CMAKE_CURRENT_LIST_DIR}/misc/cpp/imgui_stdlib.cpp
)

target_link_libraries(imgui glfw)