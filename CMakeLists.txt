add_executable(helloworld src/main.c)

target_link_libraries(helloworld
    libsel4
    libsel4printf
    libsel4startstop
)

add_dependencies(helloworld sel4_kernel)
