cmake_minimum_required(VERSION 2.6)
project( GLEW )

if(MINGW OR UNIX)
  set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wno-attributes")
endif()

include_directories( ${GLEW_SOURCE_DIR}/include )

add_library( glew STATIC src/glew.c )

source_group( include REGULAR_EXPRESSION "[.]h$" )
source_group( src     REGULAR_EXPRESSION "[.]cpp$" )
