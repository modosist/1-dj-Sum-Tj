cmake_minimum_required(VERSION 3.5)
project(Branch)

set(CMAKE_CXX_STANDARD 17)

set(SOURCE
        dlmalloc.cpp
        Job.cpp
        main.cpp
        Problem.cpp
        )

set(HEADERS
        h.h
        Job.h
        Mem.h
        Mem0.h
        Mem2.h
        Mem3.h
        Mem4.h
        Problem.h
        )

if ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "GNU")
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -march=native")
endif()

add_executable(${PROJECT_NAME} ${SOURCE} ${HEADERS})
