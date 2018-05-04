project(glfw_example)
cmake_minimum_required(VERSION 3.0)

find_package(glfw3 REQUIRED)

set(FILES
	simple.c
)

set(GLAD ./deps/glad/glad.h
         ./deps/glad.c)

if (WIN32)
    list(APPEND OPENGL_LIBRARIES opengl32)
else() # Linux
	list(APPEND OPENGL_LIBRARIES GL GLEW)
endif()

add_executable(simple ${FILES} ${GLAD})

target_include_directories(simple PUBLIC ${INCLUDE_DIRS} "./deps")
target_link_libraries(simple glfw ${LIBRARIES} ${OPENGL_LIBRARIES})
