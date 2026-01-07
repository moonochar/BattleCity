cmake_minimum_required(VERSION 4.2.1 FATAL_ERROR)

set(PROJECT_NAME BattleCity)
project(${PROJECT_NAME})

add_executable(${PROJECT_NAME} src/main.cpp)

set (GLFW BUILD DOCS OFF CACHE BOOL "" FORCE)
set(GLFW BUILD TESTS OFF CACHE BOOL "" FORCE)
set(GLFW BUILD EXAMPLES OFF CACHE BOOL "" FORCE)
set (GLFW INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} glfw)

add_subdirectory(external/glad)
target_link_libraries(${PROJECT_NAME} glad)