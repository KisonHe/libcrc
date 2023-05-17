cmake_minimum_required(VERSION 3.20)

file(GLOB LIBCRC_SOURCES
        "src/*.*"
        )

add_library(CRC STATIC
        ${LIBCRC_SOURCES}
        )

target_include_directories(CRC PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
        )
