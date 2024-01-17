add_library(cregres OBJECT)

target_sources(cregres
    PRIVATE
        regression.c
    PUBLIC
        regression.h
)
target_link_libraries(cregres PRIVATE probability)
target_include_directories(cregres PUBLIC ${CMAKE_CURRENT_LIST_DIR})

