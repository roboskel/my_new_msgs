cmake_minimum_required(VERSION 2.8.3)
project(pointcloud_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  sensor_msgs
  message_generation
)

find_package(message_generation)

 add_message_files(
   FILES
   PointCloud2_Segments.msg
 )

 generate_messages(
   DEPENDENCIES
   std_msgs
   sensor_msgs
 )


catkin_package(
	CATKIN_DEPENDS message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)



