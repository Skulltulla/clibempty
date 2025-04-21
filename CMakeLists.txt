cmake_minimum_required(VERSION 3.10.0)

set(PROJECT_NAME clibempty)
set(PROJECT_VERSION 0.1.0)

project (
    ${PROJECT_NAME} 
    VERSION ${PROJECT_VERSION} 
    LANGUAGES C
)

set (
    SOURCE_FILES 
    src/private/clibempty.c
)

add_library (
    ${PROJECT_NAME} 
    STATIC 
    ${SOURCE_FILES}
)

target_include_directories (
    ${PROJECT_NAME} 
    PUBLIC 
    ${CMAKE_CURRENT_SOURCE_DIR}/src/public
)
