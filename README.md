# FreeRTOS Application on SAM E70 Xplained Ultra Evaluation Board

This project is built off of the following GitHub repo: [Microchip-MPLAB-Harmony/core_apps_sam_e70_s70_v70_v71](https://github.com/Microchip-MPLAB-Harmony/core_apps_sam_e70_s70_v70_v71/tree/master)

## Overview

This project uses MPLAB X IDE to build a FreeRTOS application on the SAM E70 Xplained Ultra Evaluation Board. 

## Features

- **5 Tasks with Different Priorities**: Each task writes to a virtual COM Port over USART.
- **Pre-emption Enabled**: Ensures the highest priority task executes when needed.
- **Mutex and Critical State**: Used by tasks to eliminate any lockups during output writing.
- **Task 4**: Triggered by the SWD button on the board, it has the highest priority and pre-empts all other tasks.
- **Task 3**: Triggered by any key press and sends a signal over UART. If the "l" key is pressed, an LED is turned on.
- **Tasks 1, 2, and BLINK**: Write to the COM Port with the lowest of the 5 priorities, each with different delays and timings to demonstrate pre-emption.

## Task Details

- **Task 1**: Writes to the COM Port with the lowest priority.
- **Task 2**: Writes to the COM Port with a slightly higher priority than Task 1.
- **BLINK Task**: Writes to the COM Port with a priority between Task 2 and Task 3.
- **Task 3**: Triggered by any key press, with specific behavior for the "l" key.
- **Task 4**: Triggered by the SWD button, with the highest priority.

## Example Output

Below is an example image of the output:
![Example Output](https://github.com/dtriska/ATSAME70_FreeRTOSDemo/assets/112901210/2d58caa7-248d-44c7-8b54-0de949dc55d0)
