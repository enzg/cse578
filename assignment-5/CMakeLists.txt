cmake_minimum_required(VERSION 3.5.11)
project(optical-flow)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_BUILD_TYPE Debug)
find_package(OpenCV REQUIRED)
add_executable(run_of src/run_of.cpp src/optical_flow.cpp)
add_executable(run_motion_seg src/run_motion_seg.cpp src/optical_flow.cpp)
add_executable(run_tracking src/run_tracking.cpp src/optical_flow.cpp)
target_link_libraries(run_of ${OpenCV_LIBS})
target_link_libraries(run_motion_seg ${OpenCV_LIBS})
target_link_libraries(run_tracking ${OpenCV_LIBS})
