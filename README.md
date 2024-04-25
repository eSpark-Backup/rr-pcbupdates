# PCB Design porting and Troubleshooting
### Client Name: R R

## Project Description
This PCB controls a water cooling system. It uses a 12v ATX input to power the water pump, sensors, and LED lights while three PWM, 4-pin fan inputs then power three corresponding PWM, 4-pin outputs. The idea behind the PCB is to be able to control the water pump, LEDs, and fans based on some basic conditions from the sensor inputs.

If one of the following is detected, then the result is what follows:

- Flow rate equals 0, then power should be turned off for water pump and 3 PWM fans. Pump LED light switches from green to red.
- Water is detected, then power should be turned off for water pump and 3 PWM fans. Water Detection LED light switches from green to red.

Under normal conditions (when flow rate >0 and no water is detected) the pump and fans run at 100% power and both LEDs are green. We have an adjustable delay switch on the PCB that allows water to start flowing, that way the flow sensor does not read 0 and cut power as the PCB is powering up.
