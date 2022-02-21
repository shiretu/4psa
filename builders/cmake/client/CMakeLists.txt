project(client)

# make the list with all the source files
file(GLOB_RECURSE SOURCES "${SOURCES_ROOT}/${PROJECT_NAME}/src/*.cpp")

# what will be the include search path
include_directories(${SOURCES_ROOT}/${PROJECT_NAME}/src/include)

# what will we create: the static library
add_executable(${PROJECT_NAME} ${SOURCES})

# stuff linked to the executable
target_link_libraries(${PROJECT_NAME} common)
