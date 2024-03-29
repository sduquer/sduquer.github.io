---
layout: post
title: Quadcopter drone for AI applications.
permalink: /drone-ai-project/
---
This  an on-going project that can be splitted into several little projects and tasks. Through this article, i want to explain the main parts of this development, in order to show some interesting and useful solutions for various challenges that have arisen during the development to date.

FPV system with analog camera:
{% include youtube.html id='GN_3PN3ziP0' %}

<br/>
Flying...

<!-- Última actualización: {{ page.last_modified_at }} -->

<!--more-->
* Do not remove this line (it will not be displayed)
{:toc}
<!-- ##  Let's see it in action! -->
<!-- {% include youtube.html id='iUnWrxdl2SY' %} -->
<br />
##  Goals of the project

The main goal of this project, which I started during the pandemic of covid 19 about 2020, is to build an stable aerial vehicle to be used as a platform to develop and test applications of Artificial Intelligence, based on a real-time video capturing system and required hardware installed on the vehicle.

4K video camera:
{% include youtube.html id='iUnWrxdl2SY' %}

The specific objectives of the project are:
1. Building a structure capable of rising and being remotely controlled so that it moves in a specific direction / height.
2. The flight time must be sufficient to be able to carry out aerial monitoring. Flight time is restricted by different factors: total weight (which in turn is defined by the structure, motors, batteries, devices, etc.), costs, among others. For example: a battery with a higher capacity could be heavier, which in turn is closely related to the cost.
3. The design of the vehicle must allow the assembly of different devices and peripherals.
4. The flight controller must allow a standard communication protocol, so that a companion computer can talk with it. The goal is to be able to send it commands in order to guide the vehicle depending on the function it is performing.

![This is how I look like today :)](/assets/img/drone_AI/imagen_drone_vista_frontal.jpeg)

![This is how I look like today :)](/assets/img/drone_AI/imagen_drone_vista_frontal_camara.jpeg)


## What is a Quadcopter?
As defined by [OscarLiang][]:
>Quadcopter is an unmanned aerial vehicle (UAV) or drone with four rotors, each with a motor and propeller. A quadcopter can be manually controlled or can be autonomous. It's also called quadrotor helicopter or quadrotor. It belongs to a more general class of aerial vehicles called multicopter or multirotor.

Another good site is [Devopedia][]. Here you can find information about several Information Technology Topics.

[OscarLiang]: https://oscarliang.com/what-is-quadcopter/#:~:text=A%20quadcopter%20is%20a%20type,as%20surveillance%20and%20aerial%20photography.
[Devopedia]: https://devopedia.org/quadcopter

 
## Hardware
This drone was built by using the following parts:
<!-- 1. [Frame + Power Distribution Board (PDB).](#frame--power-distribution-board-pdb) -->
1. Frame + Power Distribution Board (PDB).
2. Motors.
3. ESC (Electronic Speed Controller).
4. Propellers.
5. Battery.
6. Flight Controller.
7. FPV goggles (First Person View) + OSD (On Screen Display) + Video TX.
8. Companion Computer.
9. 3D printed parts.

![My main components](/assets/img/drone_AI/imagen_componentes_fpv.jpeg)


## Challenges
1. FPV system
One the main challenges was to build the FPV system, that is used to display telemetry information on the goggles, such us: position, battery voltage, GPS, altitude, etc. It is composed by three parts, mainly:
- OSD: it overlays flight information onto the FPV video feed that is displayed on the FPV goggles. The information is sent from the Flight controller to the OSD, by using serial communication. The OSD modifies the video image, by adding the telemetry data, and sends it through the Video TX to the FPV goggles. A micro minimOSD was used for this purpose.
- Video TX: It sends the analog video stream received from the OSD by using an specific band and channel. This signal is received by the FPV goggles and displayed on the screen.
- FPV goggles: It allows the pilot to see the video captured by the camera installed on the drone. 

<!-- ### Frame + Power Distribution Board (PDB) -->
