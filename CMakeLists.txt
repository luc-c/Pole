project(pole)

set(VERSION "0.5")

add_library(pole STATIC pole/pole.h pole/pole.cpp)
target_include_directories(pole PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>/pole)
set_target_properties(pole PROPERTIES PUBLIC_HEADER "pole/pole.h")

install(TARGETS pole)   
