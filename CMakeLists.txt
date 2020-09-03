add_library(imgui STATIC
	examples/imgui_impl_sdl.cpp
    examples/imgui_impl_opengl3.cpp
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_widgets.cpp
)

add_library(imgui)

target_include_directories(imgui
	PUBLIC include
)

target_compile_definitions(imgui PRIVATE -DGLEW_STATIC)
target_compile_definitions(imgui PRIVATE IMGUI_IMPL_OPENGL_LOADER_GLEW)
