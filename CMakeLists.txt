add_library(ImGui STATIC
	examples/imgui_impl_sdl.cpp
    examples/imgui_impl_opengl3.cpp
    examples/imgui_impl_glfw.cpp
    examples/imgui_impl_glfw.h
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_widgets.cpp
)

target_include_directories(ImGui
	PUBLIC ./
    PUBLIC ./examples
)

target_compile_definitions(ImGui PRIVATE -DGLEW_STATIC)
target_compile_definitions(ImGui PRIVATE IMGUI_IMPL_OPENGL_LOADER_GLEW)

target_link_libraries(ImGui
    SDL2-static
    glew
    glfw
)