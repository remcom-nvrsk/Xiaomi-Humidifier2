# Humidifier2 -- ARDUINO ProMicro Version
Xiaomi SmartMi Evaporative Humidifier water level sensor

Thanks to Tomas Vilda for a great job with reverse engineering water sensor serial communication https://github.com/tomasvilda/humidifierstart
Thanks to yhunter's hardware (#fakcior)  https://www.youtube.com/watch?v=JudoDFqBNoU great job and Video Guide using Arduino Nano
https://github.com/fakcior/xiaomi-humidifier-water-sensor


This sketch uses Capacitive Touch Library in order to utilize existing hardware.

Solder 1M resistor between two pins on your board, I used D2 and D3, then connect/solder your board as direct replacement of the blue sensor module on the power supply PCB (5V, GND, TX, both probes, looking from the top on 2-pin header left one is sensing pin, second one is GND)
If Arduino ProMicro is used in project - Use Serial1() class for RX/TX pins and Serial() for USB Communication

Calibrate your board when fully assembled with empty and full tank then modify accordingly MIN_READING and MAX_READING definitions.

BEWARE: it is advised to calibrate by pouring the water and simultaneously monitoring the sensor value. Save the maximum one. When the water hits certain level it'll short both metal rods making the measurement returns -2. It is expected behaviour.
