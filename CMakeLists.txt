cmake_minimum_required(VERSION 3.18)

project(shortcuts 
  VERSION 1.0.0
  LANGUAGES CXX)

#-----------------------------------------------------------------------
# CPM configuration
#-----------------------------------------------------------------------
  set(MODULE_NAME shortcuts)
  
  # if ((DEFINED CPM_DIR) AND (DEFINED CPM_UNIQUE_ID) AND (DEFINED CPM_TARGET_NAME))
  #   set(CPM_LIB_TARGET_NAME ${CPM_TARGET_NAME})
  #   set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CPM_DIR})
  #   include(CPM)
  # else()
  #   set(CPM_DIR "${CMAKE_CURRENT_BINARY_DIR}/cpm-packages" CACHE TYPE STRING)
  #   find_package(Git)
  #   if(NOT GIT_FOUND)
  #     message(FATAL_ERROR "CPM requires Git.")
  #   endif()
  #   if (NOT EXISTS ${CPM_DIR}/CPM.cmake)
  #     message(STATUS "Cloning repo (https://github.com/iauns/cpm)")
  #     execute_process(
  #       COMMAND "${GIT_EXECUTABLE}" clone https://github.com/iauns/cpm ${CPM_DIR}
  #       RESULT_VARIABLE error_code
  #       OUTPUT_QUIET ERROR_QUIET)
  #     if(error_code)
  #       message(FATAL_ERROR "CPM failed to get the hash for HEAD")
  #     endif()
  #   endif()
  #   include(${CPM_DIR}/CPM.cmake)
  # endif()
  
  # Include CPM modules or externals here (with CPM_AddModule).
  
  # CPM_InitModule(${CPM_MODULE_NAME})

  # The lib itself
  add_library(${MODULE_NAME} INTERFACE)
  target_include_directories(${MODULE_NAME} INTERFACE ${PROJECT_SOURCE_DIR})
  # set_target_properties(${MODULE_NAME} PROPERTIES LINKER_LANGUAGE CXX)
  # target_include_directories(${MODULE_NAME} )
  # target_link_libraries(${CPM_LIB_TARGET_NAME} ${CPM_LIBRARIES})
