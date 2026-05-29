cmake_minimum_required(VERSION 3.31)
project("inverter_poller" LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

file(GLOB SOURCES *.cpp)
add_executable(inverter_poller ${SOURCES})
target_compile_options(inverter_poller PRIVATE -O2)

find_package(Threads REQUIRED)
target_link_libraries(inverter_poller Threads::Threads)
