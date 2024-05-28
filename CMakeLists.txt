cmake_minimum_required(VERSION 3.0)
project(FaceTracker)

# Set C++11 standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find OpenCV package
find_package(OpenCV REQUIRED)

# Add executable
add_executable(FaceTracker main.cpp)

# Include OpenCV headers for the C API
target_include_directories(FaceTracker PUBLIC ${OpenCV_INCLUDE_DIRS})

# Link OpenCV libraries
target_link_libraries(FaceTracker ${OpenCV_LIBS} vtkCommon vtkWidgets)
