cmake_minimum_required(VERSION 3.0)
project(node-addon-api  CXX)

###############
# ASI default settings
list(APPEND CMAKE_MODULE_PATH "$ENV{ASV_CMAKE}")
include(asv_cmake_defaults)
asv_cmake_defaults( )
###############

set(libname node-addon-api)

# main header file
install(
    FILES
    napi.h
    napi-inl.h
    napi-inl.deprecated.h
    src/node_api.h
    src/node_api_types.h
    DESTINATION include/${libname}
    )
