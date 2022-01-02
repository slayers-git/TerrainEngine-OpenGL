cmake_minimum_required (VERSION 3.12)
project (Terrain)

set (src
    ./Engine/Window.cpp
    ./Engine/utils.cpp
    ./Engine/shader.cpp
    ./Engine/buffers.cpp
    ./Engine/texture.cpp
    ./Engine/glError.cpp
    ./Engine/ScreenSpaceShader.cpp
    #    ./Engine/shaderUtils.cpp
    ./Engine/BaseShader.cpp
    ./DrawableObjects/GUI.cpp
    ./DrawableObjects/Skybox.cpp
    ./DrawableObjects/Terrain.cpp
    ./DrawableObjects/CloudsModel.cpp
    ./DrawableObjects/VolumetricClouds.cpp
    ./DrawableObjects/drawableObject.cpp
    ./DrawableObjects/Water.cpp
    ./Main.cpp
    ./Compile/stb_image.cpp
    ./Compile/glad.c
    ./Compile/stb_image_write.cpp
    ./imgui/imgui_draw.cpp
    ./imgui/imgui.cpp
    ./imgui/imgui_widgets.cpp
    ./imgui/imgui_impl_opengl3.cpp
    ./imgui/imgui_impl_glfw.cpp)

add_executable (TerrainGen ${src})
target_link_libraries (TerrainGen glfw)
target_include_directories (TerrainGen PUBLIC Include DrawableObjects)
