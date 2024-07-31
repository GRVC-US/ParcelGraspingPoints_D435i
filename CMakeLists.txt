cmake_minimum_required(VERSION 3.10)

project(ParcelGraspingPoints_D435i)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(ParcelGraspingPoints_D435i src/Main.cpp)

find_package(realsense2 REQUIRED)

find_package(OpenCV REQUIRED)

find_package(Eigen3 REQUIRED)

include_directories(${realsense2_INCLUDE_DIR} ${OpenCV_INCLUDE_DIRS} ${EIGEN3_INCLUDE_DIRS} ${PCL_INCLUDE_DIRS})

target_link_libraries(ParcelGraspingPoints_D435i ${realsense2_LIBRARY} ${OpenCV_LIBS} Eigen3::Eigen tinyxml2)

