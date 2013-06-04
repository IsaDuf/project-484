include_directories(${CMAKEDEMO_SOURCE_DIR}/src)
#link_directories(${CMAKEDEMO_BINARY_DIR}/src)

#add_executable(main main.cpp)

#these are all compiled the same way
set(PROGRAMS main)
set(CORELIBS ${FFTW_LIBRARY} ${LIBSNDFILE_LIBRARY} m)

foreach(program ${PROGRAMS})
  add_executable(${program} ${program}.cpp)
  target_link_libraries(${program} ${CORELIBS})
endforeach(program)
