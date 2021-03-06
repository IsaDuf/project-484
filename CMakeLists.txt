cmake_minimum_required(VERSION 2.6.4)
project(FINAL)

# FFTW
find_library(FFTW_LIBRARY
     NAMES fftw3 fftw)
set(FFTW_LIBRARIES "${FFTW_LIBRARY}")
if(UNIX AND NOT WIN32)
     find_library(FFTW_libm_LIBRARY
         NAMES m)
     list(APPEND FFTW_LIBRARIES "${FFTW_libm_LIBRARY}")
endif()

# libsndfile
FIND_PATH(LIBSNDFILE_INCLUDE_DIR sndfile.h)

SET(LIBSNDFILE_NAMES ${LIBSNDFILE_NAMES} sndfile libsndfile)
FIND_LIBRARY(LIBSNDFILE_LIBRARY NAMES ${LIBSNDFILE_NAMES} PATH)

IF(LIBSNDFILE_INCLUDE_DIR AND LIBSNDFILE_LIBRARY)
    SET(LIBSNDFILE_FOUND TRUE)
ENDIF(LIBSNDFILE_INCLUDE_DIR AND LIBSNDFILE_LIBRARY)

IF(LIBSNDFILE_FOUND)
    IF(NOT LibSndFile_FIND_QUIETLY)
        MESSAGE(STATUS "Found LibSndFile: ${LIBSNDFILE_LIBRARY}")
    ENDIF (NOT LibSndFile_FIND_QUIETLY)
ELSE(LIBSNDFILE_FOUND)
    IF(LibSndFile_FIND_REQUIRED)
        MESSAGE(FATAL_ERROR "Could not find sndfile")
    ENDIF(LibSndFile_FIND_REQUIRED)
ENDIF (LIBSNDFILE_FOUND)

# Additional Flags
set(CMAKE_CXX_FLAGS "-g -Wall")

# Directories
add_subdirectory(src)
