**Overview**

This project demonstrates how to control a stepper motor using an Arduino and a pulse-based driver (e.g., TB6600, DM860H). The motor rotates 2000 steps forward, pauses, then reverses 2000 steps backward in an infinite loop.

**Features**

Controls stepper motor rotation via PUL (pulse) and DIR (direction) pins.
Supports bidirectional movement.
Adjustable speed control using delayMicroseconds().
Includes an optional enable pin (ENA).

**File Structure**

├── stepper_motor.ino  # Arduino code for stepper motor control
├── README.md          # Project documentation

**Hardware Requirements**

Arduino Board (Uno, Mega, etc.)
Stepper Motor (NEMA 17, NEMA 23, etc.)
Stepper Motor Driver (TB6600, DM860H, etc.)
Power Supply (Matching motor voltage & current requirements)
Jumper Wires

**Wiring Diagram**

Arduino Pin          Driver Pin

6 (PUL)                PUL+
7 (DIR)                DIR+
5 (ENA)                ENA+ (Optional)
GND                    PUL-, DIR-, ENA-

**Usage Instructions**

Upload stepper_motor.ino to your Arduino.
Connect the stepper motor driver as per the wiring table.
Power on the motor driver.
The motor will rotate 2000 steps forward, pause, then reverse 2000 steps.
Adjust delayMicroseconds(500); to change speed.

**Future Improvements**

Add serial input to change speed & direction dynamically.
Implement acceleration & deceleration profiles.
Use interrupts or timers instead of delayMicroseconds().
