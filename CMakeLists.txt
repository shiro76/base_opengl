# CMake minimum version
cmake_minimum_required(VERSION 3.10)

# Nom du projet
project(OpenGL_Base)

# Version de C++ standard
set(CMAKE_CXX_STANDARD 17)

# Ajouter le répertoire des headers
include_directories(includes)
include_directories(includes/glfw/include)
link_directories(OpenGL_Base includes/glfw/lib)

# Ajout des fichiers sources
add_executable(OpenGL_Base src/main.cpp 
    src/glad.c)

target_link_libraries(OpenGL_Base glfw3)
