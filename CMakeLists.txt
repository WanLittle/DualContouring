cmake_minimum_required(VERSION 2.6)

Project(DualContouring)

file(GLOB DC_SRC "DualContouring/*.cpp" "DualContouring/*.h")

find_package(OpenGL REQUIRED)
find_package(glm REQUIRED)
find_package(SDL2 REQUIRED)
find_package(GLEW REQUIRED)

add_executable(${PROJECT_NAME} ${DC_SRC})

target_link_libraries(${PROJECT_NAME} ${OPENGL_LIBRARY} SDL2::SDL2 SDL2::SDL2main glm GLEW::GLEW)
