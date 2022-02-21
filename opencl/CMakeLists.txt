# CMakeList.txt: проект CMake для opencl; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#
cmake_minimum_required (VERSION 3.8)

# Добавьте источник в исполняемый файл этого проекта.
add_executable (opencl "opencl.cpp" "opencl.h")

# TODO: Добавьте тесты и целевые объекты, если это необходимо.
