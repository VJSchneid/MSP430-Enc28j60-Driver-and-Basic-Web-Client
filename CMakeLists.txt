cmake_minimum_required(VERSION 3.8.2)

project(enc28j60-driver)

set(SOURCE_FILES
    main.c
    spi.c
    ipstack.c
    enc28j60.c
)

add_executable(enc28j60-driver ${SOURCE_FILES})

target_compile_features(enc28j60-driver PRIVATE cxx_std_17)

target_compile_options(enc28j60-driver PUBLIC "-mmcu=msp430f5529")
target_link_options(enc28j60-driver PUBLIC "-mmcu=msp430f5529")
