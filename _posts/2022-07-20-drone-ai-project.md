---
layout: post
title: Quadcopter drone for AI applications.
---
This  an on-going project that can be splitted into several little projects and tasks. Through this article, i want to explain the main parts of this development, in order to show some interesting and useful solutions for various challenges that have arisen during the development to date.

<!--more-->


* Do not remove this line (it will not be displayed)
{:toc}
##  Let's see it in action!
{% include youtube.html id='iUnWrxdl2SY' %}



<br />
The above video shows one of the first flights of the drone.

##  Goals of the project

The main goal of this project, which I started during the pandemic of covid 19 about 2020, is to build an stable aerial vehicle to be used as a platform to develop and test applications of Artificial Intelligence, based on a real-time video capturing system and required hardware installed on the vehicle.

The specific objectives of the project are:
1. Building a structure capable of rising and being remotely controlled so that it moves in a specific direction / height.
2. The flight time must be sufficient to be able to carry out aerial monitoring. Now I know that the flight time is restricted by different factors: total weight (which in turn is defined by the structure, motors, batteries, devices, etc.), costs, among others. For example: a battery with a higher capacity could be heavier which in turn is closely related to the cost.
3. The vehicle design must allow the assembly of different devices and peripherals.
4. The flight controller must allow a standard communication protocol so that a companion computer can talk with it. The goal is to be able to send it commands in order to guide the vehicle depending on the function it is performing.

## What is a Quadcopter?
As it is defined by [OscarLiang][]:
>Quadcopter is an unmanned aerial vehicle (UAV) or drone with four rotors, each with a motor and propeller. A quadcopter can be manually controlled or can be autonomous. It's also called quadrotor helicopter or quadrotor. It belongs to a more general class of aerial vehicles called multicopter or multirotor.

Another good site is [Devopedia][]. Here you can find information about several Information Technology Topics.


[OscarLiang]: https://oscarliang.com/what-is-quadcopter/#:~:text=A%20quadcopter%20is%20a%20type,as%20surveillance%20and%20aerial%20photography.
[Devopedia]: https://devopedia.org/quadcopter

 
## Hardware
This drone was built by using the following parts:
1. [Frame + Power Distribution Board (PDB).](#frame--power-distribution-board-pdb)
2. Motors.
3. ESC (Electronic Speed Controller).
4. Propeller.
5. Battery.
6. Flight Controller.
7. FPV googles (First Person View).
8. OSD (On Screen Display).
9. Companion Computer.

### Frame + Power Distribution Board (PDB)
