---
title: "Interactive Gallery" 
date: 2018-10-07T11:17:14+02:00
publishdate: 2018-10-07T11:17:14+02:00
image: "/images/case/interactive-gallery.jpg"
tags: ["Tech", "VR"]
comments: false
---

An interactive gallery experience in partnership with Guggenheim
Abu Dhabi

#### Background

After a talk between Pierre Depaz and
the curators of Guggenheim Abu Dhabi,
we decided to work with Guggenheim Abu Dhabi and develop an interactive gallery for curators and artists. 

#### User and Audience
The target users are curators, interior designers and artists who
want to experiment with curation and exhibitions without going
through the hassle of moving physical art pieces around.

{{< vimeo 301184055 >}}

<br>

#### Team & Role
This project is a collaboration with [Nicolas White](https://www.facebook.com/nickychristmas) and
mentored by [Pierre Depaz](https://pierredepaz.net/).
I was in charge of designing and developing its core interactions, presenting 
the prototype
to the curators and managers of Guggenheim, as well as writing
documentation for future researchers.

#### Interaction Design
After a discussion, we nailed down the core interactions
as three parts: teleporting (navigating the space),
moving paintings (and sculptures), and interacting with other curators.

##### Teleporting
![](/images/case/gallery-1.jpg)
In Virtual Reality interaction design, moving around the space is not
as intuitive as in real life, because the users
will remain in the same physical space even though they
might have explored a ginormous area in VR. To allow users to check
 out a virtual space from all spots, we implemented the 
teleport functionality which the users can use to navigate the
space. Teleportation here follows the VR convention of trackpad's Point and Move.
By pressing down the controller's trackpad and swiping
it in different directions, the user can choose a spot in the gallery
and move him/herself to the spot.

##### Moving painting
![](/images/case/gallery-2.jpg)
Moving painting or sculpture around is the core interaction of the project. With the flexibility
and low cost of experimentation in VR,
curators will have great freedom to try out new layout or novel ideas
for an exhibition. The action of moving painting includes
two simple steps: to pick up a selected painting and to place
it at another place. We experimented and designed an intuitive way 
of enabling this action, basically using the trigger button
to **grab** and **drop**. 

When the user gets closer to a painting, he can
point his controller to this painting. An indicator
line will show up, connecting the painting with the controller.
If the user presses trigger at this point,
he or she will have the painting in his hand. Then the user
can teleport around the space and decide on where
this art piece belongs. He will then release the trigger,
and put this painting in place.

To improve user experience, we added a magnet interaction 
feedback: as we move around gallery, if the painting gets closer to a wall,
it will be magnetically attached to this wall (after user releases
the trigger). With this improvement, we find it easier
to hang paintings without needing to teleport super next
to a wall.

##### Interacting with other people
![](/images/case/gallery-3.jpg)
This add-on functionality enables multiple curators (who might
 be all over
the world) to connect and join the same VR session.
We used [Unity Photon Framework](https://www.photonengine.com/en/PUN)
to develop a network connection that allows multiple people
to join the gallery for a collaborative curation session. Joiners will have their
avatars inside the space of this gallery, and they can see each other's
moves or actions on-the-fly.
 
 Since traditional curation is
be a social activity with back-and-forth conversation between curators
and artists, we wanted to simulate this experience by encouraging
 virtual communication and idea exchanges in real-time.

#### More Information
See the source code [here](https://github.com/njw275/Interactive-Gallery/tree/master/paintingMoving)