cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

add_definitions(-std=c++11)

set(CXX_FLAGS "-Wall" "-pedantic")
set(CMAKE_CXX_FLAGS, "${CXX_FLAGS}")

project(ukf_augmentation_mean_covariance)

find_package(Eigen3 REQUIRED NO_MODULE)

add_executable(ukf_augmentation_mean_covariance main.cc ukf.cc)
target_link_libraries(ukf_augmentation_mean_covariance Eigen3::Eigen)