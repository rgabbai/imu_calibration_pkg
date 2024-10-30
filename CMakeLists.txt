cmake_minimum_required(VERSION 3.5)
project(imu_calibration_pkg)

# Find dependencies
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)  # ROSIDL generators for services

# Generate the custom service definition
rosidl_generate_interfaces(${PROJECT_NAME}
  "srv/CalibrateIMU.srv"
)

rosidl_generate_interfaces(${PROJECT_NAME}
  "srv/GetRPY.srv"
)

# Export dependencies
ament_export_dependencies(rosidl_default_runtime)
ament_package()
