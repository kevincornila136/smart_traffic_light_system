# Smart Traffic Light System using STM32

This project represents a small scale simulation of an adaptive traffic light system developed for learning purposes using the STM32 NUCLEO-L476RG platform. The application was implemented in STM32CubeIDE using the C programming language and the HAL library provided by STMicroelectronics.

The system controls a four-direction intersection using a finite state machine and multiple traffic light states. Vehicle detection is performed using IR sensors connected through EXTI interrupts, allowing the microcontroller to react in real time without continuous polling.

Each direction uses two sensors: a FAR sensor used for traffic counting and a NEAR sensor used for queue detection close to the intersection. Based on the detected traffic density, the application dynamically adjusts the green light duration in the next traffic cycle. A simple starvation prevention mechanism was also implemented to avoid blocking low traffic directions for long periods of time.

For debugging and monitoring, the system sends live information through UART, including active direction, sensor counters and adaptive timing values.

The project was developed as an embedded systems learning exercise focused on modular software architecture, interrupt handling, GPIO control, adaptive logic implementation and real-time debugging on STM32 platforms.
