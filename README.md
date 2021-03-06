# owenquad
Raspberry Pi based quadcopter with full walkthrough coding tutorial

originally forked from https://code.google.com/p/owenquad/

## Tutorial pages

[Full walkthrough tutorial](http://owenson.me/build-your-own-quadcopter-autopilot)

A raspberry pi quadcopter with full construction walkthrough so you can understand how everything works.

## How it works: 
All custom code and hardware except the Pi. AVR (Arduino) microcontroller used as interface board for Pi, to read RC inputs and output motor control signals (over I2C bus). Real-time attitude control (stabilisation) and input processing is done on the Pi in C++. Stabilisation algorithm is two cascaded PIDs (per axis, six total), one for angular velocity (AV-PID) and one for absolute angle feeding into the AV PID. Orientation is sensed with an MPU6050 chip from Invensence (using on-board sensor fusion).

## Goals: 
Full autonomous flight for reconnaissance, surveying farms, disaster areas, power and pipe lines, crowd monitoring, etc. Ideally with self-organising behaviour for task completion with other drones.

## Why a Raspberry Pi? 
Higher level processing, 3G connection, web cam, etc. Far more room to have complex code than a simple microcontroller. Challenges are real-time execution of control loops - which I might offload to the AVR but that will remove the ability to communicate with it over I2C (because the MPU6050 uses I2C).

## Current status: 

See video below - flies well - currently adding additional sensors for autonomous flight (compass, barometer and GPS).

## PICTURES AND VIDEO

[video](https://www.youtube.com/embed/iSKVnFI_7HA) 

![board](http://owenquad.googlecode.com/files/owenquad-intboard-sml.jpg)
