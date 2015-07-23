
add_custom_command(
    OUTPUT ../../images/helloworld-image-ia32-pc99
    COMMAND echo "hi from helloworld"
    COMMENT "Helloworld image"
)

add_executable(helloworld-main src/main.c)
target_link_libraries(helloworld-main
    ${CMAKE_BINARY_DIR}/libs/libsel4putchar/libsel4putchar.a
    ${CMAKE_BINARY_DIR}/libs/libsel4startstop/libsel4startstop.a
    ${CMAKE_BINARY_DIR}/libs/libsel4/libsel4.a
)

add_dependencies(helloworld-main
    sel4_kernel
    sel4putchar
    sel4startstop
)

