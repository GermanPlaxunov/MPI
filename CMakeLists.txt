cmake_minimum_required(VERSION 3.25)
project(openmpi_test)

set(CMAKE_CXX_STANDARD 17)

# Add MPI Package to Project
find_package(MPI REQUIRED)

add_executable(openmpi_test main.cpp openmpi_hello.cpp)

# Link MPI libraries
target_link_libraries(openmpi_test PRIVATE MPI::MPI_CXX)