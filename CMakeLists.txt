cmake_minimum_required(VERSION 3.13)
project(Paprika)
set(CMAKE_CXX_STANDARD 14)

set(SOURCE_FILES src/application.cpp)
# list(APPEND SOURCE_FILES src/otherfiles.cpp)

add_subdirectory(lib/GLFW)
find_package(OpenGL REQUIRED)

add_executable(application ${SOURCE_FILES})

target_link_libraries(application glfw)
target_link_libraries(application OpenGL::GL)