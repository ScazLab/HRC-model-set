---
title: Accompanying Software
category: Software
order: 1
---

![setup](https://user-images.githubusercontent.com/4378663/27803086-bf42338c-5ff5-11e7-976d-b0e10f0988f2.jpg)

We provide a set of software libraries for perception, control and interaction, with the goal of encouraging other researchers to proactively contribute to the proposed work.
Our software is compatible with the Robot Operating System (ROS, [[Quigley et al. 2009]](http://www.willowgarage.com/sites/default/files/icraoss09-ROS.pdf)), the most used middleware to date for robotics research and industry applications.
It has been released under the `LGPLv2.1` open-source license, and it is freely available on GitHub. The repository, available at [this link](https://github.com/scazlab/baxter_collaboration), hosts both the source code for the software library, and some example applications. It is readily available for any Baxter robot, but it is meant to be easy to extend to other robot platforms---provided a valid URDF model is available.

For the purposes of this work, we devised a set of basic capabilities in order for the robot to be an effective partner. To this end, we implemented two low-level, state-less controllers (one for each of the robot's arms) able to operate in parallel and to communicate one another if needed.
A library of high-level predefined actions (in the form of ROS services) is available for the client to choose from; such actions range from the simple, single arm `pick object` to the more complex `hold object` (which requires a physical collaboration with the human partner) or `hand over` (which demands a bi-manual interaction between the two arms). Inverse kinematics is provided by `TRAC IK` [[Beeson and Ames 2015]](http://ieeexplore.ieee.org/document/7363472/), an efficient, general-purpose library that has been adapted to the Baxter robot and guarantees a control rate of `100 Hz`.

The system allows for context-based, multi-modal interactions with the user. Multiple, redundant communication channels are exposed by the framework, with the goal of interacting with the user on _human terms_ [[Breazeal2002]](http://dlia.ir/Scientific/e_book/Technology/Engineering_Civil_Engineering_(General)/TA_166_167_Human_Engineering_/020286.pdf). This redundancy aims at allowing the human partner to choose the interface that suits him the most; importantly, it also has the advantage of making the interaction itself more robust. The exposed layers are the following:

 * **Web Interface**
it enables bi-directional communication between the robot and the human peer. It is based on `roslibjs`, a JavaScript library that interfaces with ROS [[Toris et al. 2015]](http://ieeexplore.ieee.org/document/7354021/).

 * **Feedback Channel**
it is presented to the user in the Baxter's head display (see figure). It allows the user to receive constant feedback about the robot's state and intents.

 * **Text-to-Speech (TTS) System**
based on the [SVOX-PICO engine](https://en.wikipedia.org/wiki/SVOX), is used to verbally interact with the human peer during task execution.

 * **Force Interaction Layer**
it endows the robot with the capability of detecting when a specific force pattern is applied by the human partner to the robot's arm. This is particularly important to accomplish natural interactions during physical collaborative actions (for example holding a lumber while the human drills into it).

 * **Emergency Channel**
it allows the human partner to send error messages to the controllers: it can be triggered by either pressing one of the buttons on the robot's end-effector, or by pressing an appropriate button on the web interface, if the arm is not within reach.

 * **Speech-to-Text (STT) System**
 it employs the [Google Cloud STT API](https://cloud.google.com/speech/docs/) to convert human sentences into robot-readable ROS commands in the form of ROS messages through a specific topic.

The main purpose of the accompanying software is to facilitate prospective users with the adoption of the model set in collaborative experiments.
Collectively, they target a generic human-robot collaborative setup, with the aim of equipping a standard robot with enough skills for it to effectively locate, manipulate, and interact with parts and tools.
