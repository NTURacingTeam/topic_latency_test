cmake_minimum_required(VERSION 3.0.2)
project(topic_latency_test)

find_package(Boost REQUIRED COMPONENTS date_time thread)
find_package(catkin REQUIRED COMPONENTS message_generation rostime roscpp rosconsole roscpp_serialization)

include_directories(${catkin_INCLUDE_DIRS})
link_directories(${catkin_LIBRARY_DIRS})

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime std_msgs)

foreach(dir
    tlt_listener
    tlt_talker
    )
  rostutorial(${dir})
endforeach()

install(FILES
  launch/topic_latency_test.launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)
