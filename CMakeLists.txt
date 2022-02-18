cmake_minimum_required(VERSION 3.9)
project(FaceRecognitionDemo)

set(CMAKE_CXX_STANDARD 11)
find_package( OpenCV REQUIRED ) # locate OpenCV in system
include_directories( ${OpenCV_INCLUDE_DIRS} ) # provide library headers
add_executable(FaceRecognitionDemo main.cpp)
target_link_libraries(FaceRecognitionDemo ${OpenCV_LIBS} /usr/local/lib/libopencv_core.so) # link OpenCV library
MESSAGE("OpenCV_LIBS: " ${OpenCV_LIBS} )  #display opencv libs found
