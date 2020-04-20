cmake_minimum_required(VERSION 2.8.4)
project(kalman)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# Get Eigen
# find_package(Eigen3 REQUIRED) 
# add_library(eigen INTERFACE)
# target_include_directories(eigen INTERFACE ${EIGEN3_INCLUDE_DIRS})

# Setup kf lib 
add_library( kalman kalman.cpp )

# set(SOURCE_FILES kalman.cpp kalman-test.cpp)
# add_executable(kalman-test ${SOURCE_FILES})
target_link_libraries(kalman eigen)
