project (unit-tests)
cmake_minimum_required (VERSION 2.8.3)
set(EXE unit_tests)

add_definitions(-DBOOST_TEST_DYN_LINK) 

set(SOURCE_FILES "unit_tests.cpp")
add_executable(${EXE} ${SOURCE_FILES})

include_directories(..)

find_package(Boost 1.46 REQUIRED COMPONENTS unit_test_framework)

include_directories(${Boost_INCLUDE_DIRS})
target_link_libraries(${EXE} es ${Boost_LIBRARIES})

