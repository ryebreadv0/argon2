cmake_minimum_required(VERSION 3.22.0)

project(argon2)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror")

add_library(${PROJECT_NAME} 
	src/blake2/blake2b.c
	src/argon2.c
	src/core.c
	src/encoding.c
	src/ref.c
	src/thread.c
)

set(ARGON2_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/include)

target_include_directories(${PROJECT_NAME}
	PUBLIC ${ARGON2_INCLUDE_DIR}
)

