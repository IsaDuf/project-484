include_directories(${CMAKEDEMO_SOURCE_DIR}/src)
#link_directories(${CMAKEDEMO_BINARY_DIR}/src)

#the one C file
add_executable(main main.c)

#these are all compiled the same way
#set(PROGRAMS oglfirst pointers)
set(CORELIBS ${FFTW_LIBRARY} m)

foreach(program ${PROGRAMS})
  add_executable(${program} ${program}.cpp)
  target_link_libraries(${program} ${CORELIBS})
endforeach(program)
