include_directories(${catkin_INCLUDE_DIRS})
add_executable(tlt_listener tlt_listener.cpp)
target_link_libraries(tlt_listener ${catkin_LIBRARIES})
install(TARGETS tlt_listener
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
