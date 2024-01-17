add_library(netlib OBJECT)

target_sources(netlib
    PRIVATE
        erfunc.c
#       stl.c
    PUBLIC
        erfunc.h
#       stl.h
)
target_link_libraries(netlib PRIVATE )
target_include_directories(netlib PUBLIC ${CMAKE_CURRENT_LIST_DIR})

