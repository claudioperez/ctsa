
set(SOURCE_FILES
          autoutils.c
					boxcox.c
					boxjenkins.c
					ctsa.c
					emle.c
					filter.c
					initest.c

					pred.c
					talg.c
					errors.c
					unitroot.c
					seastest.c
#				spectrum.c
)

set(HEADER_FILES
          autoutils.h
					boxcox.h
					boxjenkins.h   	
					ctsa.h
					emle.h
					filter.h
					initest.h

					pred.h
					talg.h
					errors.h
					unitroot.h
					seastest.h
#				spectrum.h
#				waveletarima.h
)
#include_directories(${CMAKE_CURRENT_SOURCE_DIR} ./hsfft ./optimc ./netlib ./wavelib ./cregres)
add_subdirectory(hsfft)
add_subdirectory(optimc)
add_subdirectory(netlib)
add_subdirectory(wavelib)
add_subdirectory(polynomial)
add_subdirectory(probability)
add_subdirectory(cregres)

add_library(ctsalib STATIC ${SOURCE_FILES} ${HEADER_FILES})

target_link_libraries(ctsalib PUBLIC
                      hsfft
                      optimc
                      netlib
                      wavelib
                      cregres
                      polynomial
                      probability)
        
set_property(TARGET ctsalib PROPERTY FOLDER "lib")

target_include_directories(ctsalib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

