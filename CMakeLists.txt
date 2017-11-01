cmake_minimum_required(VERSION 3.1)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON) 
set(CMAKE_CXX_EXTENSIONS OFF)

#set(EXTRA_BINCFLAGS "-Wall -Wextra")
#set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} ${EXTRA_BINCFLAGS})

project (PlaceDescriptionService)
add_subdirectory(/Users/noesis/Projects/place_description_service/googletest)
include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})
include_directories(/Users/noesis/Projects/soundex/googletest/googlemock/include)

set(sources /Users/noesis/Projects/place_description_service/)
set(sources ${sources}/PlaceDescriptionServiceTest.cpp)
add_executable(PlaceDescriptionServiceTest ${sources})
target_link_libraries(PlaceDescriptionServiceTest gtest_main)
