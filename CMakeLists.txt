cmake_minimum_required(VERSION 2.6.4)
project(FINAL)

find_library(FFTW_LIBRARY
     NAMES fftw3 fftw)
set(FFTW_LIBRARIES "${FFTW_LIBRARY}")
if(UNIX AND NOT WIN32)
     find_library(FFTW_libm_LIBRARY
         NAMES m)
     list(APPEND FFTW_LIBRARIES "${FFTW_libm_LIBRARY}")
endif()

set(CMAKE_C_FLAGS "-g -Wall")
add_subdirectory(src)
