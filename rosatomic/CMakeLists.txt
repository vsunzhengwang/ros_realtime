cmake_minimum_required(VERSION 2.8.3)
project(rosatomic)
find_package(catkin REQUIRED )

catkin_package(
    DEPENDS # TODO add dependencies
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS include include/boost include/ros # TODO include
    LIBRARIES # TODO
)
include_directories(include ${catkin_INCLUDE_DIRS})
catkin_add_gtest(utest test/utest.cpp)


install(DIRECTORY include/ros include/boost DESTINATION ${CATKIN_GLOBAL_INCLUDE_DESTINATION})

#install(DIRECTORY include/ DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION})

#install(DIRECTORY test/ DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
