project("imgui" LANGUAGES C CXX)

file(GLOB src
    imconfig.h
    imgui.h
    imgui.cpp
    imgui_tables.cpp
    imgui_draw.cpp
    imgui_internal.h
    imgui_widgets.cpp
    imstb_rectpack.h
    imstb_textedit.h
    imstb_truetype.h
    imgui_demo.cpp
    backends/imgui_impl_opengl3.h
    backends/imgui_impl_opengl3.cpp
    backends/imgui_impl_glfw.h
    backends/imgui_impl_glfw.cpp
)

add_library(imgui STATIC ${src})

target_include_directories(imgui
    PUBLIC
    .
    ../GLFW/include
)

