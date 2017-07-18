cmake_minimum_required(VERSION 3.7)

SET (SOURCES "footswitch.cpp" "common.cpp" "common.h" "debug.cpp" "debug.h")

if (WIN32)    
	INCLUDE_DIRECTORIES("E:/apps/hidapi-0.7.0/hidapi")
    find_library(HIDAPI_LIB hidapi PATHS "E:/apps/hidapi-0.7.0/windows/Debug")
endif (WIN32)

add_executable(footswitch ${SOURCES})
target_link_libraries(footswitch ${HIDAPI_LIB})