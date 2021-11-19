include_directories(${catkin_INCLUDE_DIRS})
add_executable(tlt_talker tlt_talker.cpp)
target_link_libraries(tlt_talker ${catkin_LIBRARIES})
install(TARGETS tlt_talker
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
