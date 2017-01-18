
cmake_minimum_required(VERSION 2.8)

ADD_DEFINITIONS(-g)
 
project(Registration)
 
find_package(ITK REQUIRED)
include(${ITK_USE_FILE})
 
add_executable(Registration MACOSX_BUNDLE DeformableRegistration.cxx)
target_link_libraries(Registration ${ITK_LIBRARIES})
