
# STM32 FreeRTOS Project

## Overview

This repository contains a project that ports the latest FreeRTOS to an STM32 microcontroller, providing a real-time operating system for embedded applications. It is intended to help developers create, test, and deploy embedded applications using FreeRTOS and STM32 microcontrollers.

## Features

- **FreeRTOS Version**: Latest release ported to STM32
- **Hardware Platform**: [Specify your STM32 model, e.g., STM32F4/F7/H7/L4 series]
- **IDE/Toolchain**: [Mention your development environment, e.g., STM32CubeIDE, Keil, IAR, GCC with CMake, etc.]
- **Supported Features**:
  - Task creation and management
  - Interrupt and ISR handling
  - FreeRTOS configuration for timers, queues, and semaphores
  - Integration with peripheral drivers (e.g., UART, I2C, SPI)

## Getting Started

### Prerequisites

To build and run this project, you will need:

- [STM32 development board] (Specify model)
- [Toolchain, e.g., STM32CubeIDE, GCC ARM Embedded Toolchain, etc.]
- A [debugger/programmer, e.g., ST-LINK V2/V3]

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/duvitech-llc/stm32-freertos.git
   ```
2. Open the project in your preferred IDE (e.g., STM32CubeIDE) or prepare your build system (CMake, Makefiles, etc.).

### Building and Running

1. Configure the project for your target STM32 microcontroller.
2. Connect your STM32 board to the PC.
3. Build the project and flash it using the provided scripts or the IDE's built-in functionality.

### Project Structure

```
stm32-freertos/
├── Core/              # Main application code
|   |── Startup/       # Startup files
│   ├── Src/           # Source files
│   ├── Inc/           # Header files
├── External/          # External Library Source
|   ├── FreeRTOS/      # FreeRTOS Kernel source files
|   │   ├── Source/    # FreeRTOS core files
|   │   ├── Config/    # FreeRTOS configuration files (FreeRTOSConfig.h)
├── Drivers/           # STM32 peripheral drivers (HAL/LL)
└── README.md          # Project documentation (This file)
```

### Configuration

- **FreeRTOSConfig.h**: This file contains the configuration parameters for FreeRTOS such as task priorities, stack sizes, tick rate, and more.
- **SystemClock_Config()**: Make sure the system clock is correctly configured for your application needs.

### Usage

- To create a new FreeRTOS task, use:
  ```c
  xTaskCreate(taskFunction, "TaskName", stackSize, pvParameters, priority, &taskHandle);
  ```
- To use semaphores, queues, or other FreeRTOS mechanisms, refer to [FreeRTOS Documentation](https://www.freertos.org/documentation.html).

### Troubleshooting

- Ensure your system clock settings match your STM32's specifications.
- Verify that the FreeRTOS heap settings (heap_1, heap_2, etc.) are suitable for your application.
- Debug issues using the integrated debugger in your IDE.

