PROJECT(patl)
CMAKE_MINIMUM_REQUIRED (VERSION 2.6)
INCLUDE (CMakeMacro.cmake)

SET(CMAKE_C_FLAGS "-Wno-error")
SET(CMAKE_CXX_FLAGS "${CMAKE_C_FLAGS}")

AUX_SOURCE_DIRECTORY(uxn/patl SRC_PATL)
ADD_LIBRARY(patl SHARED ${SRC_PATL})
INSTALL (TARGETS patl DESTINATION ${LIBDIR})

