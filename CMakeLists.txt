cmake_minimum_required(VERSION 3.16)
project(learnopengl)

# Add all src/*.cpp and src/*.c to project
file(GLOB project_sources "src/*.cpp" "src/*.c")
add_executable(learnopengl ${project_sources})

# Set headers location
include_directories(${CMAKE_SOURCE_DIR}/include)

# Set libraries location
target_link_libraries(learnopengl ${CMAKE_SOURCE_DIR}/lib/GLFW/libglfw3.a)

add_compile_options(-lglfw3 -lGL -lX11 -lpthread -lXrandr -lXi -ldl)
#target_link_libraries(learnopengl ${CMAKE_DL_LIBS})