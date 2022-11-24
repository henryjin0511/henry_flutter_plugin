# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(henry_flutter_plugin_library VERSION 0.0.1 LANGUAGES C)

add_library(henry_flutter_plugin SHARED
  "henry_flutter_plugin.c"
)

set_target_properties(henry_flutter_plugin PROPERTIES
  PUBLIC_HEADER henry_flutter_plugin.h
  OUTPUT_NAME "henry_flutter_plugin"
)

target_compile_definitions(henry_flutter_plugin PUBLIC DART_SHARED_LIB)
