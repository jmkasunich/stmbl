![Build Status](https://travis-ci.org/rene-dev/stmbl.svg)
[![Join the chat at https://gitter.im/rene-dev/stmbl](https://badges.gitter.im/rene-dev/stmbl.svg)](https://gitter.im/rene-dev/stmbl?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Build Log: https://travis-ci.org/rene-dev/stmbl

DISCLAIMER
===

THE AUTHORS OF THIS SOFTWARE ACCEPT ABSOLUTELY NO LIABILITY FOR
ANY HARM OR LOSS RESULTING FROM ITS USE.  IT IS _EXTREMELY_ UNWISE
TO RELY ON SOFTWARE ALONE FOR SAFETY.  Any machinery capable of
harming persons must have provisions for completely removing power
from all motors, etc, before persons enter any danger area.  All
machinery must be designed to comply with local and national safety
codes, and the authors of this software can not, and do not, take
any responsibility for such compliance.

This software is released under the GPLv3.

stmbl
=====

IMPORTANT:  This fork should **NOT** be used to make PC boards.
The board layout files have been reverted to work with the stable version of Kicad, which affects the copper.  At some point I will probably clean up the resulting issues, but that is not a priority.  I simply want to be able to view the layout using the stable version.


There is a wiki. https://github.com/rene-dev/stmbl/wiki
There will be documentation.

**IRC: #stmbl on irc.hackint.eu**
https://webirc.hackint.org/#stmbl

stmbl is an open source servo drive designed for Retrofitting CNC machines and Robots. It supports Industrial AC and DC servos with up to 320V and 2kW (see [specs](https://github.com/rene-dev/stmbl/wiki/specs) for details).

Documentation about the PCB and pinout of the feedback connector:

https://github.com/rene-dev/stmbl/wiki/Pinouts

https://github.com/rene-dev/stmbl/wiki/PCB

##### Hardware version 4.0
![top](http://rene-dev.github.io/IMG_2017-03-05%2022:08:03.jpg)
![bot](http://rene-dev.github.io/IMG_2017-03-05%2022:07:44.jpg)

##### Driving a Bosch Turboscara
https://www.youtube.com/watch?v=d6NH1W7DUnQ

##### Driving a Manutec Robot
https://www.youtube.com/watch?v=gwgnAeGjZrA  
https://www.youtube.com/watch?v=wXLcAZwjlzE

##### Drivetest
https://www.youtube.com/watch?v=-E1o_5cFyto

#### Supported Motors
* Synchronous AC Servos
* DC Servos
* 2 Phase HF spindle motors
* IRAMX Hardware testet up to 320V

#### Supported Feedback systems
* Resolvers
* Incremental encoders
* sin/cos encoder interpolation
* Mitsubishi absolute encoders
* Sanyo Denki absolute encoders
* Yaskawa absolute encoders
* Sick HIPERFACE®

##### Planned:
* EnDat
* BiSS
* SSI
* Sanyo Denki wire-saving incremental encoder

#### Supported Position/Velocity Commands Inputs:
* Smartserial
* Quadrature
* Step/direction
* RS485

#### TODO
* AC Async

#### Directories
* hw/eagle/ Eagle board files and schematics
* hw/spice/ Spice simulation for resolver interface
* src/ STM32F4 code, command, feedback and control loop
* stm32f103/ STM32F1 code, running on the HV side, generating PWM
* bootloader/ bootloader for the f4
