cmake_minimum_required(VERSION 3.12)

# Способ 1
# Задать путь к Pico SDK перед подключением файла pico_sdk_import.cmake
set(PICO_SDK_PATH "c:\\App\\Raspberry Pi\\Pico SDK v1.5.1\\pico-sdk\\")

# Способ 2: Передача пути к SDK как параметра командной строки при вызове CMake
# cmake -DPICO_SDK_PATH=/home/assets/rasberry-pi-pico/pico-sdk

# Name project
SET(ProjectName apkSpiUarts)

# Set any variables required for importing libraries
SET(FREERTOS_KERNEL_PATH ${CMAKE_CURRENT_SOURCE_DIR}/lib/FreeRTOS-Kernel)

# Import those libraries
include(pico_sdk_import.cmake)
include(${FREERTOS_KERNEL_PATH}/portable/ThirdParty/GCC/RP2040/FreeRTOS_Kernel_import.cmake)

# Define project
project(${ProjectName})

# Initialize the Raspberry Pi Pico SDK
pico_sdk_init()

# Add subdirectories
add_subdirectory(src)

# if you have anything in "lib" folder then uncomment below - remember to add a CMakeLists.txt
# file to the "lib" directory
#add_subdirectory(lib)