cmake_minimum_required(VERSION 4.2.1 FATAL_ERROR)

set(PROJECT_NAME BattleCity)

project(${PROJECT_NAME})

add_executable(${PROJECT_NAME} src/main.cpp)

set (GLFW BUILD DOCS OFF CACHE BOOL "" FORCE)
set(GLFW BUILD TESTS OFF CACHE BOOL "" FORCE)
set(GLFW BUILD EXAMPLES OFF CACHE BOOL "" FORCE)
set (GLFW INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)


# Линкуем GLFW
target_link_libraries(${PROJECT_NAME} glfw)