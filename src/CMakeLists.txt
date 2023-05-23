cmake_minimum_required (VERSION 3.15)

include ("math/CMakeLists.txt")

set (CODER_HEADER 
    "coder.h" 
    "${CODER_MATH_HEADER}" 
     )
set (CODER_SRC 
    "coder.cpp" 
    "${CODER_MATH_SRC}" 
     )
list (APPEND CODER_SRC "${CODER_HEADER}")

add_library(coder STATIC "${CODER_SRC}")