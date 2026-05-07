Project Description

This project demonstrates a smart fan control system built using the STM32 Nucleo development board and an ultrasonic sensor for human presence detection. The system is designed to automatically control a fan based on whether a person is present in a defined area. The ultrasonic sensor continuously measures the distance to detect the presence of a person, and the STM32 microcontroller processes this data to control the fan accordingly. When a person enters the detection range, the fan is turned ON, and when the person leaves the area, the fan is turned OFF after a short delay. This project illustrates an energy-efficient automation system that eliminates unnecessary power consumption.

Objectives

The main objectives of this project are to interface an ultrasonic sensor with the STM32 microcontroller for presence detection, implement control logic for automatic switching of a fan, reduce energy consumption through intelligent automation, and demonstrate real-time embedded system control using sensor input and GPIO output.

Hardware Used

The hardware components used in this project include the STM32 Nucleo Development Board, an HC-SR04 Ultrasonic Sensor, a DC fan (or motor), a motor driver module or transistor (for switching the fan), jumper wires, a breadboard, and a power supply. The STM32 acts as the controller, the ultrasonic sensor detects presence, and the fan acts as the output device.

Pin Configuration

The ultrasonic sensor’s TRIG pin is connected to PA1 configured as a GPIO output, and the ECHO pin is connected to PA2 configured as a GPIO input. The fan control pin is connected to PA5 and configured as a digital output, which drives the motor driver or transistor circuit to switch the fan ON or OFF.

System Functionality

The system continuously monitors the distance using the ultrasonic sensor. The STM32 sends a trigger pulse to the sensor, and the echo response is measured to calculate the distance between the sensor and any object. When a person is detected within a predefined threshold distance (for example, 100 cm), the system interprets it as presence detection and turns the fan ON by setting the output pin HIGH. The time of detection is recorded using the internal system timer. If no object is detected for a specified duration (for example, 5 seconds), the system turns the fan OFF automatically. This ensures that the fan operates only when needed, thereby conserving energy.

Output Behavior

The output is observed through the operation of the fan. When a person enters the detection area, the fan starts running, and when the person leaves, the fan stops after a delay. This behavior provides a clear demonstration of automated control based on real-time sensing.

Software Details

The project is implemented in C using STM32CubeIDE. STM32 HAL libraries are used to configure and control GPIO pins and timers. The ultrasonic sensor interfacing is handled using precise timing logic, while the fan control is achieved using digital output signals. Timing functions such as system ticks are used to implement delay-based decision-making.
