cmake_minimum_required(VERSION 3.0.2)
project(nav_no_obstacles)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  cv_bridge
  image_transport
  pcl_conversions
  pcl_ros
  roscpp
  rosgraph_msgs
  rospy
  std_msgs
)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)
find_package(OpenCV 4 REQUIRED)

catkin_package(
  INCLUDE_DIRS include
  LIBRARIES nav_no_obs
  CATKIN_DEPENDS roscpp rospy std_msgs image_transport cv_bridge rosgraph_msgs pcl_conversions pcl_ros
)

###########
## Build ##
###########


include_directories(
 include ${realsense_INCLUDE_DIR} ${catkin_INCLUDE_DIRS} ${OpenCV_INCLUDE_DIRS}  
)



#############
## Install ##
#############



#############
## Testing ##
#############

## Add folders to be run by python nosetests
# catkin_add_nosetests(test)
#add_executable(dotMex_Car_Cplusplus src/glwindow.cpp src/main.cpp src/image_processing.cpp)
add_executable(nav_no_obstacles src/main.cpp)
target_link_libraries(nav_no_obstacles PUBLIC Threads::Threads ${catkin_LIBRARIES} ${OpenCV_LIBS})
