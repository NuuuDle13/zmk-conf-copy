cmake_minimum_required(VERSION 3.13.1)
find_package(Zephyr HINTS $ENV{ZEPHYR_BASE})
project(keyball39)

# Add the Keyball39 source files
target_sources(app PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/src/keyball39.c
    ${CMAKE_CURRENT_SOURCE_DIR}/src/pmw3360.c
)

# Add the PMW3360 driver
target_include_directories(app PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/drivers/pmw3360)
