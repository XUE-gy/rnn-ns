cmake_minimum_required(VERSION 3.17)
project(rnnnoiseModule)

set(CMAKE_CXX_STANDARD 14)

#add_executable(speexModule main.cpp)
if(MSVC)
    SET(CMAKE_CXX_FLAGS "/utf-8" "${CMAKE_CXX_FLAGS}")    # for CPP
    SET(CMAKE_C_FLAGS "/utf-8" "${CMAKE_C_FLAGS}")        # for C
endif(MSVC)

aux_source_directory(./src  CPPLIST)

add_executable(
        ${PROJECT_NAME}
        ${CPPLIST}
        #rnnoise_demo.c
        rnnnoise_improve_demo2.c
)





target_include_directories( ${PROJECT_NAME}
        PRIVATE
        ${PROJECT_SOURCE_DIR}/include
        ${PROJECT_SOURCE_DIR}/src
        )

