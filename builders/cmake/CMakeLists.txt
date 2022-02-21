# we have to have modern cmake
cmake_minimum_required(VERSION 3.0)

# the name of the project
project(all)

# establish folder structure
get_filename_component(PROJECT_ROOT "../.." ABSOLUTE)
get_filename_component(BUILDER_ROOT "${PROJECT_ROOT}/builders/cmake" ABSOLUTE)
get_filename_component(SOURCES_ROOT "${PROJECT_ROOT}/sources" ABSOLUTE)
message(STATUS "PROJECT_ROOT: ${PROJECT_ROOT}")
message(STATUS "BUILDER_ROOT: ${BUILDER_ROOT}")
message(STATUS "SOURCES_ROOT: ${SOURCES_ROOT}")

# add our 3 projects which are:
# 1. a common library
# 2. the server
# 3. the client
add_subdirectory(common)
add_subdirectory(server)
add_subdirectory(client)

