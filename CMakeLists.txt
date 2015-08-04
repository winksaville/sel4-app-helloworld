set(target "helloworld")

add_executable(${target} src/main.c)

target_link_libraries(${target}
    libsel4
    libsel4printf
    libsel4startstop
)

AddRunTarget(${target})

add_dependencies(${target} sel4_kernel)
