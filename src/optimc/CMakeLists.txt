add_library(optimc OBJECT)

target_sources(optimc
    PRIVATE
        brent.c
        conjgrad.c
        lls.c
        lnsrchmp.c
        matrix.c
        neldermead.c
        newtonmin.c
        nls.c
        stl.c
        optimc.c
        secant.c
    PUBLIC
        brent.h
        conjgrad.h
        lls.h
        lnsrchmp.h
        matrix.h
        neldermead.h
        newtonmin.h
        nls.h
        stl.h
        optimc.h
        secant.h
)
target_include_directories(optimc PUBLIC ${CMAKE_CURRENT_LIST_DIR})

