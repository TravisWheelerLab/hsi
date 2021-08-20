cmake_minimum_required(VERSION 3.12)
project(
        hsi
        VERSION 1.0.0
        HOMEPAGE_URL https://github.com/TravisWheelerLab/hsi
)

set(CMAKE_C_STANDARD 17)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY build)

add_executable(
        sindex

        src/sindex.c
        src/hsi_index.c
)
target_link_libraries(sindex m)
install(TARGETS sindex RUNTIME)

add_executable(
        sstat

        src/sstat.c
        src/hsi_index.c
)
target_link_libraries(sstat m)
install(TARGETS sstat RUNTIME)

add_executable(
        sfetch

        src/sfetch.c
        src/hsi_index.c
)
target_link_libraries(sfetch m)
install(TARGETS sfetch RUNTIME)
