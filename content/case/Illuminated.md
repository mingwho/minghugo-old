---
title: "Illuminated"
date: 2018-10-07T11:17:14+02:00
publishdate: 2018-10-07T11:17:14+02:00
image: "/images/case/illuminated.jpg"
tags: ["Tech", "VR", "3D Modeling"]
comments: false
---

An adventurous and thrilling first person shooter VR game.

#### Okay, so: what is Illuminated?
Illuminated is an adventurous and thrilling first person shooter VR experience. It inverts your expectations on usual shooter games: instead of seeing and shooting the opponents, you have to illuminate the environment to uncover the position of the other players before taking the killing shot.

Playing with the concept of lighting and visibility, Illuminated merges intense action and stealth game play in a novel way. The environment itself is visible but you cannot fully see it. While another person might be present, you cannot see him or her without casting a light either. Illuminated allows you to see part of the environment layout but that’s not the whole picture - pun intended.

{{< vimeo 301187277 >}}

<br>

#### Specific Moment
Picture the beginning of the match. The lights have just gone out, and the short glimpse you had of the other players is now gone. You start moving around, as you realize your opponents could have gone basically anywhere. You look around, look at your weapon, and look around again. You fire, only to realize your weapon produces light: the details in the arena around you become visible, but so do you. Before you know it, you see a projectile coming your way - someone has seen you. You teleport out of the way, trying to outsmart your foe and wondering where they might have gone next. You fire, and - Aha! Your guess was right: you see your opponent right where you wanted them. Before they realize what’s going on, you make your attack. Your shot connects, but this isn’t over. You teleport out of the light into the safety of your featureless environment, ready to plan your next assault.


#### Team & Role
Illuminated is developed in collaboration
with [Mateo Molina](http://www.mateocodes.art/hi.html), [Shantanu Bhatia](http://shantanubhatia.io/) and [Grace Huang](https://www.instagram.com/thatgracehuang/).
I was in charge of project management, user interaction design (visual, audio and spatial), 
gaming logic development as well as user testing.

#### Illuminated Visual Aesthetic Inspiration
We want to create a low-poly surreal art style, to feed into the emotions of unease and unfamiliarity we wish to evoke in the players. We have used Blender and 3ds Max to make 3D models and texture shaders for lighting mechanisms.


![](/images/case/illuminated-moodboard.png)

#### Sonic environment
Our soundscape is calm, atmospheric, and not constant or overwhelming, but rather eventful and event-based. Music and ambient sounds fit the stark and surreal aesthetic of the space. Sound effects should be short and linked to specific key event. Sound effects triggered by player(s)’ actions, like projectile collisions, grenade explosions, being illuminated etc. We want to have a more ‘discrete’ feel to them than the music, featuring a sharp attack and a quick decay that lasts only as long as the event they are tied to.


#### Core Interactions
The core interaction revolves around shooting and illuminating the world around you. The two acts are inextricably linked: the act of shooting is bound to the act of illuminating, as each weapon has both its own shooting and illuminating mechanics. You don’t have a weapon and a light: your weapon is the light. When placed in an environment that is featureless unless illuminated, along with other players that are out to hunt you, these linked mechanics mean your strengths and weaknesses are bound to a single action. You need to shoot to hunt the other players, and you need to shoot to light up the space and reveal their positions, but that same light can also expose you and leave you vulnerable. Given that player are individual actors avoiding one another, the act of searching the space with your light will always be a tense and rewarding interaction, for at any moment you can find your next target - or they can find you.

![](/images/case/bracelets.png)
<div class='image-info'>
In Illuminated, lambpost signifies a spawning
point and lights up the spawn room as an initial scene. 
Bracelets on players' hands 
display colors that indicate health values.
</div>



#### Level Map Design
Our level map design went through 3 phases.

From the simple room 
with two walls and one obstacle for the ease of development and testing
, till the last version of full on complexity and intricacy with four spawn rooms,
curvy walls (for grenade bounces), special lighting, mysterious graffiti, as well
as tons of turns and corners for players to hide and develop strategies. 

Level map phase 1

![](/images/case/level-map-1.png)

Level map phase 2

![](/images/case/level-map-2.png)

Level map phase 3

![](/images/case/level-map-3.png)

#### What is something unique about Illuminated?
“The thrill is in the chase, never in the capture” - Doctor Who

The core concept of the experience is that we hide players’ existences at first but they will have to reveal themselves when exploring the environment or finding others. In this way, the weapon also becomes a weakness: shooting or lighting up others exposes players themselves too.

The concept of exposing both yourself and your opponents provides a blend of action and stealth gameplay. Often, action and stealth mechanics in games do not cooperate, but coexist. Sneak around unless you’re spotted and then gun down your enemies. Or defeat everyone in sight so that you may slip back into the shadows. One mechanic is employed until it outlives its usefulness, then gives way to the other. Illuminated challenges this relationship by combining its action and stealth elements into a single mechanic. Attacking and hiding are intertwined within the act of shooting: the attack is the stealth.





#### More Information

Check out the source code [here](https://github.com/mjm973/Illuminated). Read our [project proposal](https://github.com/mjm973/Illuminated/blob/master/project_proposal.md),
 or [tech specifications](https://github.com/mjm973/Illuminated/blob/master/technical_specifications.md).