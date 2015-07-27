add_executable(helloworld-main src/main.c)

target_link_libraries(helloworld-main
    libsel4
    libsel4printf
    libsel4startstop
)

add_dependencies(helloworld-main sel4_kernel)
