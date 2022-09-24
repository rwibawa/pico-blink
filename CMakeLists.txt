cmake_minimum_required(VERSION 3.14)

# initialize the SDK based on PICO_SDK_PATH
include(pico_sdk_import.cmake)

project(blink C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

set(PICO_EXAMPLES_PATH ${PROJECT_SOURCE_DIR})

# initialize the Pico SDK
pico_sdk_init()

# create executable 'blink'
add_executable(blink
  blink.c
)

# Pull in our pico_stdlib which pulls in commonly
target_link_libraries(blink
  pico_stdlib
)

# create map/bin/hex file etc.
# the output is 'blink.uf2'
pico_add_extra_outputs(blink)