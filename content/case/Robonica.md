---
title: "Robonica"
date: 2018-10-07T11:17:14+02:00
publishdate: 2018-10-07T11:17:14+02:00
image: "/images/case/robonica.jpg"
tags: ["Tech", "Arduino"]
comments: false
---

A robotic telepresence research project that allows you
to move around the robot and explore a remote space from your phone.

A simple motorized platform with an on-board Linux computer (Raspberry Pi) and bidirectional audio and video capabilities (screen/camera, loudspeaker/microphone).

The computer runs a web server. Remote visitors access the robot's URL (e.g. from a browser on their phone) and are are presented with a basic teleconferencing system:
the image from the camera on the robot is visible on the screen of the phone. Similarly with the audio.


{{< vimeo 302513762 >}}

<br>


#### Team & Role
This project is in collaboration with Professor [Michael Shiloh](https://nyuad.nyu.edu/en/academics/divisions/arts-and-humanities/faculty/michael-shiloh.html).
I was in charge of researching the literature review of telepresence
robots, designing and developing the user interface,
gathering user feedback and writing the project documentation.

#### Overall System Design
![](/images/case/robonica-sketch.jpg)

The hardware components of Robonica include: a Raspberry Pi,
an Arduino, a 4K web camera, a digital display, 2 motors, power banks,
as well as some wood and metal pieces. 

When we were designing all the hardware parts of Robonica, 
we wanted to make sure that the system is stable and powerful enough
to go through some oblique surfaces,
all components are integrated by wires firmly,
 and also the robot will be able to walk on its own
 without being plugged into an external power supply on the wall.
 

As for the software design, we started off with 
an idea of a telepresent robot that would show the viewer's
face on its digital display, while also showing the
viewer what its camera is seeing in real life. It will 
be a bi-directional telepresence robot. However, as deadline was approaching,
we couldn't find out the way of accessing a phone's camera
from the phone's browser. So we ended up focusing on building
a minimum viable product, which was to make sure visitors on the
website would see what the robot was seeing in real time.

The software for this robot composes of two major tasks:

(1) User can control the motors from clicks
on the website.

(2) The server streams high-quality live videos
to all the clients.

I was involved in the initial research on how to make
sure both parts work separately and also together
later.
We first tried to set up a server with Python Flask
but couldn't find a way to serve both the video stream
and customer control on the same page with Raspberry
Pi.
In the end, we opted for Node.JS as backend server,
running the website, displaying video stream and allowing visitor to control
the movements.
For the video stream, we employed another server to serve
 it internally,
and the main Node server will access this video from a specific 
endpoint. 

After some sleepless nights and lots
of trial and error, we got this robot running
as how we planned and showcased it
to the general public. Quite a few visitors were
interested in running the robot and learning
how we designed it.

#### Outcome
Robonica has been hanging out at NYUAD's Arts Center
and waiting for people on the NYU network to have fun
 with it :)

See the [source code](https://github.com/michaelshiloh/telepresence)