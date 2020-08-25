set(CMAKE_POLICY_DEFAULT_CMP0074 NEW)
cmake_minimum_required(VERSION 3.10)
project(SOIL)

set(INC
        ${CMAKE_CURRENT_SOURCE_DIR}/include/SOIL/SOIL.h
        ${CMAKE_CURRENT_SOURCE_DIR}/include/SOIL/image_dxt.h
        ${CMAKE_CURRENT_SOURCE_DIR}/include/SOIL/image_helper.h
        ${CMAKE_CURRENT_SOURCE_DIR}/include/SOIL/stb_image_aug.h
        ${CMAKE_CURRENT_SOURCE_DIR}/include/SOIL/stbi_DDS_aug.h
        ${CMAKE_CURRENT_SOURCE_DIR}/include/SOIL/stbi_DDS_aug_c.h
        ${CMAKE_CURRENT_SOURCE_DIR}/include/SOIL/SOIL.h
        )

set(SRC
        ${CMAKE_CURRENT_SOURCE_DIR}/src/image_dxt.c
        ${CMAKE_CURRENT_SOURCE_DIR}/src/image_helper.c
        ${CMAKE_CURRENT_SOURCE_DIR}/src/stb_image_aug.c
        ${CMAKE_CURRENT_SOURCE_DIR}/src/soil.c
        )

add_library(SOIL STATIC ${SRC} ${INC})

target_include_directories(SOIL PUBLIC
        "${PROJECT_SOURCE_DIR}/include")