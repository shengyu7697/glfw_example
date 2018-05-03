project(glfw_example)
cmake_minimum_required(VERSION 3.0)

find_package(glfw3 REQUIRED)

set(FILES
	simple.c
)

set(GLAD ./deps/glad/glad.h
         ./deps/glad.c)

add_executable(simple ${FILES} ${GLAD})

target_include_directories(simple PUBLIC ${INCLUDE_DIRS} "./deps")
target_link_libraries(simple opengl32 winmm glfw ${LIBRARIES})
#target_link_libraries(simple GL GLEW glfw ${LIBRARIES})
