cmake_minimum_required(VERSION 3.12)
project(contiki_ng)

set(CMAKE_C_STANDARD 90)

# set include path
include_directories(os)
include_directories(arch/platform/sky)
include_directories(arch/cpu/msp430)

# set project files
set(DEV_PROJECT_PATH project)
file(GLOB_RECURSE src_list
        "${DEV_PROJECT_PATH}/*.h"
        "${DEV_PROJECT_PATH}/*.c")

add_executable(contiki_ng ${src_list})