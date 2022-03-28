# CMakeList.txt: проект CMake для opencl; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.

cmake_minimum_required (VERSION 3.8)

project(opencl)

# Добавьте источник в исполняемый файл этого проекта.
add_executable (opencl "code_load.cpp" "code_load.h" "data_to_raw.h" "data_to_raw.inl" "error_treatment.cpp" "error_treatment.h"
"gemm.h" "main.cpp" "openclwrap.cpp" "openclwrap.h" "useful_vector_funcs.h" "useful_vector_funcs.inl")



find_package(OpenCL REQUIRED)
target_include_directories(opencl PUBLIC ${OpenCL_INCLUDE_DIRS})
message("MESSAGE:")
message(${CMAKE_CURRENT_SOURCE_DIR})
message(${OpenCL_LIBRARY})
message("A")
link_directories(${OpenCL_LIBRARY})


target_include_directories (opencl PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(opencl PUBLIC ${OpenCL_INCLUDE_DIRS})
target_link_libraries (opencl ${OpenCL_LIBRARY})