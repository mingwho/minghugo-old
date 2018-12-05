---
title: "Interactive Human Digital Avatar"
date: 2018-10-07T11:17:14+02:00
publishdate: 2018-10-07T11:17:14+02:00
image: "/images/case/toia.jpg"
tags: ["Tech", "Chatbot"]
comments: false
---

A bilingual (Arabic-English) conversational avatar, similar to a chat bot, except that the avatar is based on pre-recorded videos of an actual human being.
The system is designed to allow anybody, simply using a laptop, to create an avatar of themselves.  As an interactive tool,  TOIA can serve as a conversational medium of story telling, thus enabling cross-cultural and cross-generational sharing and preservation of stories.  


{{< vimeo 301181868 >}}

<br>

#### Background

How do we overcome the temporal limitations of human interactivity?

Assume this is the great great grandmother of mine, but there is
no way for me to travel back in time and talk to her face-to-face
and ask her about
her experience. This project, inspired by the 
[New Dimensions in Testimony](http://ict.usc.edu/prototypes/new-dimensions-in-testimony/) at USC,
aims to create an intellectual human digital avatar that
allows time-offset interactions between the avatar and users.

<p align="center">
  <img src="/images/case/arabic-lady.jpg">
</p>

#### Team & Role
This project is mentored by Professor
 [Nizar Habash](https://nyuad.nyu.edu/en/academics/divisions/science/faculty/nizar-habash.html).
I worked with a team of five other developers on this project. 
My role was to develop the overall system from scratch
 and make sure all components integrate smoothly.
I was also responsible for the user interaction design.

#### Overall System Design

The system design includes four components: (1) a recorder
that records the avatar maker’s videos, (2) a
database that contains the avatar’s video responses
and other data facilitating the matching of the
interactor’s questions with the avatar’s answers,
(3) a player interface through which the interactor
is able to interact with the avatar, and (4) a dialogue
manager that matches the user’s speech to
the avatar’s answers in any of the four language
pairs.

![](/images/case/toia-system-design.png)
<div class='image-info'>
Overall system design contains a recorder, a database and a player.
</div>
<br>
#### Avatar Recorder
![](/images/case/avatar-recorder.png)

We implemented a web-based recorder to help
avatar makers record personal videos. The
tech stack I have used includes Node.JS, Express,
WebRTC library and MangoDB. 

The overall framework is as follows: 

Avatar
makers create scripts consisting of pairs of questions
and answers from scratch or customize existing
scripts by removing or adding questions as
desired. These scripts are uploaded to a Cloudant
database. Throughout the recording, avatar makers
can further update answers, delete questions or
add questions on the spot.
The avatar maker selects a specific question
prompt in any order and proceeds to record a video
response to pair with it. A semi-transparent head
location indicator is provided to help the avatar
maker create consist videos. The avatar maker can
review the recorded video, re-record it or delete it.


By the end of project, we have recorded four digital avatars,
three in English and one in
Arabic, each consisting of around 300 question-answer
pairs.

#### Avatar Player
![](/images/case/four-avatar.png)

The main TOIA system interface is the player,
through which the user is able to interact
with the avatar. 

Similarly as the recorder,
we implemented a web-based user interface using
Python Flask as back-end framework. It fetches
speech recognition text from Google Speech API, and
feeds the data to the dialogue manager.

![](/images/case/choose-language.png)

The user can initiate a conversation with any of the available avatars by selecting one of 
them, and then specify whether the interaction will
be in Arabic or English. The character can easily
be switched at any point by returning to the
player’s main page, after which the interaction session
would restart with a different avatar. The
player listens to the user through a microphone
and then passes the collected audio through
an ASR system (Google Speech API). The text
produced through ASR is then passed on to the
dialogue management system. The dialogue management
system returns a video file path to be displayed
by the player. While the video is playing,
the microphone switches to mute mode to avoid
feedback. It then starts listening for questions
again once the video ends.

#### Outcome
<p align="center" class='image-info'>
  <img src="/images/case/rashid.gif">
  <br>
  One of our avatars is an Arabic speaker Rashid.
</p>


This project was presented at the National Exhibition Center
 of Abu Dhabi, and also the Special Interest Group on Discourse and Dialogue
 (SIGDIAL) Conference
 in Melbourne 2018.
  
  The [project paper](http://aclweb.org/anthology/W18-5027) is published on ACL.

#### More Information
See the source code [here](https://github.com/nizarhabash1/TOIA-NYUAD)