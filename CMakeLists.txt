cmake_minimum_required(VERSION 3.14)
project(qtHelloWorld)

set(CMAKE_CXX_STANDARD 11)

# Required if: 1) using macOS and 2) using Brew
set(CMAKE_PREFIX_PATH "C:\\Qt\\5.9.9\\mingw53_32\\lib\\cmake")

# Find includes in corresponding build directories
set(CMAKE_INCLUDE_CURRENT_DIR ON)
# Instruct CMake to run moc automatically when needed.
set(CMAKE_AUTOMOC ON)

# Find the QtWidgets library
find_package(Qt5Widgets)

# Tell CMake to create the helloworld executable
add_executable(qtHelloWorld main.cpp MainWindow.cpp MainWindow.h)
#add_executable(qtHelloWorld WIN32 main.cpp)

# Use the Widgets module from Qt 5.
target_link_libraries(qtHelloWorld Qt5::Widgets)