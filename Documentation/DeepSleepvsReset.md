# Deep Sleep vs Reset

## Purpose

Determine if it is lower cost (in terms of power) to put the ESP32 into a deep sleep mode or to hold the reset line low.  This will determine the best way to put the ESP32 to sleep.

## Environment

* Erase the STM32 using STM32CubeProgrammer
* Write the ESP32 Deep sleep application to the ESP32 chip.  The application is configured to go to sleep and wait for an external GPIO to wake up the processor.
* Hardware Meadow F7 Micro V2.a

The Deep sleep application for the ESP32 can be found in the [ESP32DeepSleep](../Sources/ESP32DeepSleep) directory.

## Results

The power consumptions measurements were made twice over a 30 second period:

* When the deep sleep application is running and the ESP32 is asleep
* When the reset pin on the ESP32 is connected to ground.

Average current consumption in deep sleep: 31.42 mA

Average current consumption in reset: 32.77 mA
