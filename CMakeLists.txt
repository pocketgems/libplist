cmake_minimum_required(VERSION 3.3.2)
project(libplist)

### libplist ###

add_library(libplist
    libcnary/list.c
    libcnary/node_list.c
    libcnary/cnary.c
    libcnary/node.c
    src/bplist.c
    src/time64.c
    src/xplist.c
    src/plist.c
    src/bytearray.c
    src/ptrarray.c
    src/hashtable.c
    src/base64.c
)

target_include_directories(libplist
    PUBLIC
        include/
    PRIVATE
        libcnary/include/
        src/
)

target_compile_definitions(libplist
    PUBLIC
        -DPACKAGE_STRING="libplist 2.0.0"
)

target_link_libraries(libplist)
