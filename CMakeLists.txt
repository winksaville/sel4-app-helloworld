add_custom_command(
    OUTPUT ../../images/helloworld-image-${ARCH}-${PLAT}
    COMMAND echo "hi from helloworld"
    COMMENT "Helloworld image"
)

add_executable(helloworld-main src/main.c)

target_link_libraries(helloworld-main
    sel4startstop
    sel4putchar
    ${CMAKE_BINARY_DIR}/libs/libsel4/libsel4.a
)

add_dependencies(sel4startstop sel4_kernel)
