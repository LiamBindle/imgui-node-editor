add_library(ImGuiNodeEditor STATIC
            crude_json.cpp
            imgui_canvas.cpp
            imgui_node_editor.cpp
            imgui_node_editor_api.cpp)
add_compile_definitions(IMGUI_IMPL_OPENGL_LOADER_GLAD) # needed for header files too
target_compile_definitions(ImGuiNodeEditor PUBLIC IMGUI_IMPL_OPENGL_LOADER_GLAD)
target_include_directories(ImGuiNodeEditor PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(ImGuiNodeEditor PUBLIC ImGui)
add_library(ImGuiNodeEditor::ImGuiNodeEditor ALIAS ImGuiNodeEditor)