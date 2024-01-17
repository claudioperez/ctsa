add_library(wavelib OBJECT)

target_sources(wavelib
    PRIVATE
        wavefilt.c
        wavelib.c
        wtmath.c
    PUBLIC
        wavefilt.h
        wavelib.h
        wtmath.h
)
target_link_libraries(wavelib PUBLIC hsfft)
target_include_directories(wavelib PUBLIC ${CMAKE_CURRENT_LIST_DIR})

