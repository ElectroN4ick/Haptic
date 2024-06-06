cmake_minimum_required(VERSION 3.10)

project(Haptic VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add source files
set(SOURCES
    src/main.cpp
    src/lexer.cpp
    src/parser.cpp
    src/interpreter.cpp
    # add other source files here
)

# Add header files
set(HEADERS
    include/lexer.h
    include/parser.h
    include/interpreter.h
    # add other header files here
)

# Add the executable
add_executable(HapticExecutable ${SOURCES} ${HEADERS})
set_target_properties(HapticExecutable PROPERTIES OUTPUT_NAME "haptic")

# Include directories
target_include_directories(HapticExecutable PRIVATE include)

# Add any additional compiler flags
target_compile_options(HapticExecutable PRIVATE -Wall -Wextra -pedantic)
