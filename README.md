

# Whistler
### What is it?
A small handheld device that precisely mimics the tone and volume of a HID RFID card readers
### Why?
Often times on Red Team engagements, you will gain access to a building via tailgating. Sometimes, if the employees are well trained, they will turn around and ask you to make sure you badge in if they don't see the movement and/or hear the characteristic beep of a card read.
### Design
The design of the latest version is a very simplistic circuit. I use an RC circuit to control the timing of a 555 timer which controls an NPN transistor hooked up to a Star Micronics TMB-05. The RC circuit controls the discharge of the capacitor for a precise amount of time. I'v measured the beep time on a number of readers and they all seem to be ~250ms. I've replicated the beep time fairly precisely as seen on my oscilloscope:
![Scope Reading](https://github.com/atucom/Whistler/blob/master/Scope_timing.png)

### Bill of Materials:
For Revision E:
* 1x 2.2 Mega Ohm Resistor
* 1x 1.0 Kilo Ohm Resistor
* 2x 0.1uF Capacitor
* 1x TMB-05
* 1x 555 Timer
* 2x CR1220 Coin Cell Batteries
* 1x Pushbutton
* 2x CR1220 Coin Cell Holders
* 1x NPN Transistor

![Board Layout](https://github.com/atucom/Whistler/blob/master/Board_layout_RevE.png)