cmake_minimum_required(VERSION 3.10)
project(btt C)

# Add source files
set(BTT_SOURCES
    src/BTT.c
    src/DFT.c
    src/STFT.c
    src/Filter.c
    src/Statistics.c
    src/fastsin.c
)

# Create library
add_library(btt STATIC ${BTT_SOURCES})

# Include directories
target_include_directories(btt PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/src
) 