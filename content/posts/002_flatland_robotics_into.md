+++
date = '2025-08-18'
draft = false
title = '002_flatland_robotics_into'
#tags = [
#    "continuum robotics",
#    "serial robot",
#    "quaternions",
#    "complex number",
#    "dual quaternions",
#    "smoothness",
#    "screw theory"
#]
categories = "General"
+++


# Flatland Robotics: Intro

From an educational viewpoint, robotics can be taught in many ways. 
Flatland Robotics is an attempt to follow a different path, a different angle, a different pedagogy.
This might be a path that resonates with you or that doesn't resonate with you.
Most of the blog posts are tutorials; others are on the philosophical side.
By writing about the basics and translating the common explanations into the flatland, we will inevitably learn, gain mental clarity, and eventually uncover new thoughts. 
Writing compels us to think and provides the opportunity to reflect on the topic and its analogy to Flatland.


## So, what is Flatland Robotics about?

A [novella by Edwin Abbott Abbott (1884)](https://en.wikipedia.org/wiki/Flatland) and countless toy examples in robotics textbooks served as an inspiration for Flatland Robotics. 
In this context, Flatland is a world describing a plane.
If you want to be fancier, the Task space of Flatland is $SE(2) = E(2)\times SO(2)$.
So, the liberating vision is being able to enter robotics, start with a simple setting, and get exposed to the core ideas.

If you have ever worked on problems in $SE(3)$, you probably experienced that most of the knowledge is hidden behind highly sophisticated mathematics, such as Lie algebra, geometric algebra, and so on.
In most, if not all, cases, the troublemaker here is $SO(3)$, while the $E(3)$ part of $SE(3)$ is quite tractable and straightforward.
Ever notice that most approaches are limited to position, where orientation is either not mentioned at all or excused for future work?
Instead of working out the solution in $SO(3)$, we will derive the solution for $SO(2)$, which will provide the necessary intuition for the higher-dimensional problem.

Furthermore, understanding methods in higher dimensions may seem difficult, as they are built on [_"shut up and calculate"_](https://en.wikipedia.org/wiki/N._David_Mermin) machinery involving, among other things, high-dimensional vector spaces and heuristics.
Flatland Robotics is also an attempt to shed light on complex approaches by investigating toy examples, where 2d images are easier to digest.
Especially for beginners from mechanical engineering, computer science, electrical engineering, or mathematics, who lack the understanding of the other fields, can profit from a proper foundation in their adjacent field. 
Robotics is a multi-disciplinary field after all.

Many of the theoretical frameworks and concepts are challenging to grasp.
Therefore, to familiarize ourselves with those concepts and ideas, we should make things simple and consider the $SE(2)$ case first.
On the way, we might invent theoretical frameworks for $SE(2)$ and lower-dimensional spaces.
We should note that there are several rules in $SE(3)$ that differ from those in $SE(2)$.
Therefore, we should not expect that all approaches in a lower-dimensional space can be reformulated into higher-dimensional spaces in a one-to-one manner and vice versa.
Nevertheless, I believe that laying the foundation in Flatland will be beneficial for understanding modern approaches and primary tools in robotics.


## In a nutshell

For the lover of bullet points, here is a list. 
The list covers certain topics, including continuum robotics.
The points provide an overview, but the topics are not limited to them.

- Intuition pump:
  - from 2d flat space to 3d spatial space

- Considered robotic fields:
  - classical serial-kinematic robotics
  - continuum robotics
  - mobile and humanoid robotics

- Fun with mathematics:
  - from complex number to quaternion
  - from hyper-complex numbers to dual-quaternions
  - matrix multiplication and trigonometric functions

- Topics in robotics:
  - automatic modelling
  - kinematics, statics, and dynamics
  - algorithm for path planning
  - trajectory generation
  - control theory
  - standard textbook material and beyond


## Some series

While most of the blog posts are unorganized, I plan to group several of them into short series. 
I plan to have a series on _"Understanding Rotations,"_ _"Dynamics,"_ _"Kinematics,"_ _"Control Theory,"_ _"Smooth Trajectory Generation,"_ and _"Notes on Hypercomplex Numbers."_