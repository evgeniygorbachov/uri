cmake_minimum_required(VERSION 3.8)
set(This UriTests)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

set(Sources
    src/UriTests.cpp
)

add_executable(${This} ${Sources})

set_target_properties(${This} PROPERTIES
    FOLDER Tests
)

target_include_directories(${This} PRIVATE ..)

target_link_libraries(${This} PRIVATE Uri ${CONAN_LIBS})

add_test(
    NAME ${This}
    COMMAND ${This}
)