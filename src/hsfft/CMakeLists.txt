add_library(hsfft OBJECT)
target_include_directories(hsfft PUBLIC ${CMAKE_CURRENT_LIST_DIR})

target_sources(hsfft
    PRIVATE
        conv.c
        hsfft.c
        real.c
    PUBLIC
        conv.h
        hsfft.h
        real.h
)

