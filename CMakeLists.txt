# Needed for 3.21 
cmake_minimum_required(VERSION 3.21)

# Project name and meta information
project(
	ExampleProject
	VERSION 0.1.0
	DESCRIPTION "Example CMake project with VCPKG and Catch2" 
	LANGUAGES CXX)

option(BUILD_TESTING "Build the tests" ON)

# Only do if main project else ignore
if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)

# Testing starts here
	if(BUILD_TESTING)
		enable_testing()
		add_subdirectory(test)
	endif()
endif()





