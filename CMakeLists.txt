cmake_minimum_required(VERSION 3.21)

PROJECT(dmnameof)

LIST(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
INCLUDE(cmake/ModuleImport.cmake)
INCLUDE(cmake/ModuleCompileOptions.cmake)
ModuleSetCompileOptions()


InterfaceImport("dmnameof" "include" "")

if(PROJECT_IS_TOP_LEVEL)
    ExeImport("test" "dmnameof")
endif()

