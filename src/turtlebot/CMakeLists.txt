cmake_minimum_required(VERSION 3.8)
project(turtlebot)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)
find_package(ament_cmake_python REQUIRED)
find_package(rclpy REQUIRED)
find_package(nav_msgs REQUIRED)

ament_python_install_package(script)

install(PROGRAMS
  script/occupancy_grid_pub.py
  script/entity_spawner.py
  script/maze_solver.py
  DESTINATION lib/${PROJECT_NAME}
)

install (DIRECTORY config DESTINATION share/${PROJECT_NAME}/)
install (DIRECTORY launch DESTINATION share/${PROJECT_NAME}/)
install (DIRECTORY worlds DESTINATION share/${PROJECT_NAME}/)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  set(ament_cmake_copyright_FOUND TRUE)
  set(ament_cmake_cpplint_FOUND TRUE)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
