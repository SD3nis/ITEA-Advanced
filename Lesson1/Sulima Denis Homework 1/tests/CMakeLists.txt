CMAKE_MINIMUM_REQUIRED(VERSION 3.1)

PROJECT(DENIS)

set (DENIS_ROOT_DIRECTORY ${PROJECT_SOURCE_DIR})

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake_modules)

include(AddGMock)
add_gmock()

set (DENIS_OUTPUT_DIRECTORY_NAME bin)
set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${DENIS_ROOT_DIRECTORY}/${DENIS_OUTPUT_DIRECTORY_NAME})
set (CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${DENIS_ROOT_DIRECTORY}/${DENIS_OUTPUT_DIRECTORY_NAME})
set (CMAKE_LIBRARY_OUTPUT_DIRECTORY ${DENIS_ROOT_DIRECTORY}/${DENIS_OUTPUT_DIRECTORY_NAME})

set (DENIS_DIRECTORY ${DENIS_ROOT_DIRECTORY}/unit_tests)

add_subdirectory(unit_tests DENIS_DIRECTORY)
