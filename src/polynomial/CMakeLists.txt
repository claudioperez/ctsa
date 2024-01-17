add_library(polynomial OBJECT)

target_sources(polynomial
    PRIVATE
        polyroot.c
    PUBLIC
        polyroot.h
)

target_include_directories(polynomial PUBLIC ${CMAKE_CURRENT_LIST_DIR})

