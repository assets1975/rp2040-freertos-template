# rp2040-freertos-template

This is a template project for developing FreeRTOS based applications on Raspberry Pi RP2040 based boards. This template uses the "official" RP2040 port from the Raspberry Pi Foundation. My previous repo used the generic Cortex M0 port so this one corrects that. Previous Repo retained as tutorials rely on it.

Unmodified, this project will spawn a single task to rapidly blink the LED on and off.


# Нужно указать путь к PICO SDK.

# Способ 1

# Задать путь к Pico SDK перед подключением файла pico_sdk_import.cmake

set(PICO_SDK_PATH "c:\\App\\Raspberry Pi\\Pico SDK v1.5.1\\pico-sdk\\")

# Способ 2

# Передача пути к SDK как параметра командной строки при вызове CMake

# cmake -DPICO_SDK_PATH=/home/assets/rasberry-pi-pico/pico-sdk
