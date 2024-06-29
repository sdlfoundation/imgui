cmake_minimum_required(VERSION 3.29.6)
project(ImGui)

file(GLOB IMGUI_SRC
    backends/wiiu/imgui_impl_gx2.cpp
    imgui.cpp
    imgui_draw.cpp
    imgui_widgets.cpp
    imgui_tables.cpp
    imgui_demo.cpp
)

add_library(imgui STATIC ${IMGUI_SRC})

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
