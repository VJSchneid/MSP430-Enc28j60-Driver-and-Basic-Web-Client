cmake_minimum_required(VERSION 3.12)

project(enc28j60-driver)


add_library(config INTERFACE)

target_compile_features(config INTERFACE cxx_std_20)

target_compile_options(config INTERFACE "-mmcu=msp430f5529")
target_link_options(config INTERFACE "-mmcu=msp430f5529")

target_include_directories(config INTERFACE "include/")

add_subdirectory(src)
