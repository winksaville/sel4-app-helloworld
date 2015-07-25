add_executable(helloworld-main src/main.c)

target_link_libraries(helloworld-main
    libsel4
    sel4startstop
    sel4putchar
)

add_dependencies(helloworld-main sel4_kernel)
