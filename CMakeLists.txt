cmake_minimum_required(VERSION 2.8)
project(sqlite3_test_cpp)

SET(INCLUDE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/indclude)
SET(SOURCE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/src)

set(SOURCES
  ${SOURCE_PATH}/main.c
  #${SOURCE_PATH}/shell.c
  ${SOURCE_PATH}/sqlite3.c
)

include_directories(
  ${INCLUDE_PATH}
)			

set(LIBS
  dl
  pthread
)

add_executable(${PROJECT_NAME} ${SOURCES})
target_link_libraries(${PROJECT_NAME} ${LIBS})

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)