cmake_minimum_required(VERSION 3.10)
project(OmniBackend)

set(CMAKE_CXX_STANDARD 17)

# Include Crow and Asio headers
include_directories(
  /opt/homebrew/Cellar/crow/1.2.1.2/include
  /opt/homebrew/opt/asio/include
  ${CMAKE_SOURCE_DIR}/src
)

# Get all .cpp files in src/
file(GLOB SOURCES "src/*.cpp")

# Build the executable
add_executable(server ${SOURCES})
