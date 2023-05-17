cmake_minimum_required(VERSION 3.20)

file(GLOB LIBCRC_SOURCES
        "src/*.*"
        )

add_library(CRC STATIC
        ${AT32_DRIVER_SOURCES}
        "cmsis/cm4/device_support/system_at32f403a_407.c"
        "cmsis/cm4/device_support/startup/gcc/startup_at32f403a_407.s"
        )

target_include_directories(AT32 PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/drivers/inc
        ${CMAKE_CURRENT_SOURCE_DIR}/cmsis/cm4/device_support
        ${CMAKE_CURRENT_SOURCE_DIR}/cmsis/cm4/core_support
        ${CMAKE_CURRENT_SOURCE_DIR}/core
        )
