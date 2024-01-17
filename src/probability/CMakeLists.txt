add_library(probability OBJECT)

target_sources(probability
    PRIVATE
        dist.c
        pdist.c
        stats.c
    PUBLIC
        dist.h
        pdist.h
        stats.h
)
target_link_libraries(probability PUBLIC netlib polynomial hsfft optimc)
target_include_directories(probability PUBLIC ${CMAKE_CURRENT_LIST_DIR})

