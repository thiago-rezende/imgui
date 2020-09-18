project(DearImGui
        VERSION 1.7.8
        DESCRIPTION "Bloat-free Graphical User interface for C++ with minimal dependencies"
        HOMEPAGE_URL "https://github.com/ocornut/imgui"
        LANGUAGES CXX)


set(IMGUI_INCLUDE_DIRS
    ${CMAKE_CURRENT_SOURCE_DIR}
)

set(IMGUI_HEADERS
    "imgui.h"
    "imconfig.h"
    "imgui_internal.h"
    "imstb_rectpack.h"
    "imstb_textedit.h"
    "imstb_truetype.h"
)

set(IMGUI_SOURCES
    "imgui.cpp"
    "imgui_demo.cpp"
    "imgui_draw.cpp"
    "imgui_widgets.cpp"
)

add_library(imgui ${IMGUI_SOURCES} ${IMGUI_HEADERS})

target_include_directories(imgui PUBLIC ${IMGUI_INCLUDE_DIRS})
