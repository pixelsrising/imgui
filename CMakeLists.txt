add_library(imgui STATIC
	examples/imgui_impl_sdl.cpp
    examples/imgui_impl_opengl3.cpp
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_widgets.cpp
)

target_include_directories(imgui
	PUBLIC ./
)

target_compile_definitions(imgui PRIVATE -DGLEW_STATIC)
target_compile_definitions(imgui PRIVATE IMGUI_IMPL_OPENGL_LOADER_GLEW)

target_link_libraries(imgui
    SDL2-static
)