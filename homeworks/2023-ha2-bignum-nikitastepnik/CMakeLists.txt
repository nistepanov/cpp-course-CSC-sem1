cmake_minimum_required (VERSION 3.8)

project(bignum)

set(CMAKE_CXX_STANDARD 20)

if(MSVC)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /WX") # CMake already contains W3 in its flags
else()
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Werror -Wextra-semi -O1 -g -fsanitize=address -fno-omit-frame-pointer")
endif()

add_executable(smoke_test
    smoke_test.cpp
    bignum.hpp
        smoke_test.cpp smoke_test.cpp smoke_test.cpp smoke_test.cpp smoke_test.cpp)
