# Find Catch2 package from VCPKG
find_package(Catch2 CONFIG REQUIRED)

set(UnitTests "${CMAKE_PROJECT_NAME}_tests")

add_executable(${UnitTests}
	main.cpp
	example-test.cpp)

target_link_libraries(${UnitTests} PRIVATE Catch2::Catch2)

include(Catch)
catch_discover_tests(${UnitTests})