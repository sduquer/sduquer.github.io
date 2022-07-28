---
layout: post
title: Quad-copter drone for AI applications
---
This  an on-going project that can be splitted into several little projects and tasks. Through this article i want to explain the main parts of the development in order to show some interesting and useful solutions for various challenges that have arisen during the development to date.

<!--more-->

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



