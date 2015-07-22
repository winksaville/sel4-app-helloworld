
add_custom_command(
    OUTPUT ../../images/helloworld-image-ia32-pc99
    COMMAND echo "hi from helloworld"
    COMMENT "Helloworld image")

add_custom_target(
    helloworld-main ALL
    SOURCES src/main.c)

add_dependencies(helloworld-main sel4_kernel sel4putchar)

#add_custom_target(
#    helloworld-image ALL
#    DEPENDS helloworld-main ../../images/helloworld-image-ia
#    COMMENT "libsel4 library")
