set(SOURCE_FILES
    main.c
    spi.c
    ipstack.c
    enc28j60.c
)

add_executable(enc28j60-driver ${SOURCE_FILES})
target_link_libraries(enc28j60-driver PUBLIC config)
