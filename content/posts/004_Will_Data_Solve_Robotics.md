---
title: "Will Data Solve Robotics?"
date: 2025-09-12
description: My two cents on the latest debate on model-based versus data-based
categories: ["Opinion"]
tags: ["philosophy of science", "blue sky", "learning-based", "model-based"]
toc: true
math: true
draft: false
---




I like debates at robotics conferences. 
The first one I attended was back in 2019 in Montreal.
Actually, it wasn't the first one ever, but it's the one I remember vividly.
During the IEEE ICRA 2019, there was an interesting and funny event entitled [Debates on the Future of Robotics Research](https://starslab.ca/workshops/icra_2019_debates/), which has a part on deep learning in robotics.
Unfortunately, no video recordings of the 2019 debate.
However, you can find a RAM article of this debate and video recordings from the subsequent debates on [Robotics Debates](https://www.roboticsdebates.org/past-debates).

IEEE ICRA 2025 followed up with a spicy and dedicated debate on a similar topic.
Ken Goldberg came up with a catchy description: 
_"Will the future of robotics and automation be written in code or in data?
Is the Handbook of Robotics obsolete?
Are home humanoids overhyped?
Join us for a high-voltage debate about physics vs pixels, theory vs terabytes."_
Questioning of our bible, the Handbook of Robotics, fells like an attack on our beloved go-to reference book.
And, the combination and contrast in "physics versus pixels" and "theory versus terabytes" promise a fun debate.
I heard that debate was well attended.
It was one of the discussions we had in a team meeting and during lunchtime in my former lab.
I did not go to this conference this year, but some students in the lab attended the conference.

Luckily for us, this debate titled _"Data Will Solve Robotics and Automation: True or False"_ is [on YouTube](https://youtu.be/PfvctjoMPk8).
You should be able to see it right now.
{{< youtube PfvctjoMPk8 >}}
It is [one of the most viewed videos on the RAS YouTube channel](https://www.youtube.com/@ieee-ras/videos).
(as of writing: third highest; by the end of 2025: probably on the second spot; in the coming years: it has the potential to take the first position.)



## Some Notes on This Debate and Accompanying Article

To represent the two extreme sides of the spectrum between the classical model-based approaches and the revaling data-driven approaches,
three well-known researchers in the field of robotics for each side accepted the challenge.
The challenge was to pitch the assigned side in a three-minute presentation, defend the strong opinion, and gradually switch to their personal opinion in a Q&A with the live audience and their closing remarks.
While all six have similar personal perspectives and respect for hybrid approaches, suggesting their position somewhere in the middle of the spectrum, it was refreshing to see them present steelman arguments from opposite ends of the spectrum.
It's not exactly are steelman, but they presented the most powerful or well-constructed version of an argument to highlight their allocated extreme positions.
It kinda reminds me of the [Six Thinking Hats](https://en.wikipedia.org/wiki/Six_Thinking_Hats) methods and [devil's advocate](https://en.wikipedia.org/wiki/Devil%27s_advocate).
I'm a strong believer in productive discussions and examining extreme sides in order to find the stability of your own stance.

The presentations and discussions were playful teasing between the two extreme groups and casually picking on comments in previous presentations.
Any assertions were welcomed by the audience and I also had to chuckle.
For example, Daniela Rus' attack using they claim this and that followed by _"let me suggest that they read more papers"_ was countered by Aude Billard responding with _"Not only do we not need more data, but we don't need more papers."_
Those moments are hilarious.
Another treat is showing videos of demos, illustrating the current state of robotics and the long way it has come.

In the following, I will compress their opinion and add some comments to it.
It goes without saying; their own positions are more nuanced.


### Animesh Garg

Animesh Garg highlights that robotics is a community of communities with fractured approaches.
However, for the _"first time in many years, data provides a solution to this,"_ data-driven approaches unify those approaches _"building a common foundation base."_
This leads to a natural conclusion that _"we have to do a lot of empirical work before we can do science again."_
In other words, data is currently the way forward and a necessary step before deriving the ultimate goal of elegant, interpretable, and efficient solutions.
So, for complex tasks, empirical data must precede modeling efforts, otherwise, we will experience _"analysis paralysis"_ due to all the constraints.


### Aude Billard

[Aude Billard](https://en.wikipedia.org/wiki/Aude_Billard) reminds everyone that humanity's quest is a quest of understanding.
Data is an important part towards understanding and, it comes first in the process.
However, her _"The point is, data is needed, but it is insufficient on its own.
The true thing that may help solve part of robotics is the model."_

She made an analogy using the dataset as a library and each data point as a book.
In my understanding, opening the book is like discovering the underlying knowledge of the data point.
So, from reading and understanding the book, we can extract and construct a model to generalize the knowledge.
She mentioned that _"data without models are just data and models is what convey understanding."_
Another analogy made by her is related to teaching; students don't need more examples, they need good ones to facilitate understanding.

At the end, data is needed, but it is the quality of the data that makes a different.
_"It's not the quality that matters.
It is the differential.
It is the new data that gives you new information"_
Therefore, scaling is a wasteful approach.


###  Daniela Rus

[Daniela Rus](https://en.wikipedia.org/wiki/Daniela_Rus) has two main messages.
First, the real world is messy. 
The model-based approaches relying on first principles can only model simple specific classes of problems and work for simple constraint tasks.
Therefore, data-based approaches utilizing real-world data will help.
In fact, data is already making a difference.

Her second message is that _"there are models and models"_, stressing that robotics will require different types of learning-based models.
What can work in LLMs and vision, will not necessarily translate to good approaches for robotics.
For example, transformers are not suitable.
However, new approaches like the so-called state-space models have recurrences, enabling temporal spatial correlations, are not data hungry, and are more energy efficient.


### Leslie Kaelbling

For [Leslie Kaelbling](https://en.wikipedia.org/wiki/Leslie_P._Kaelbling), intelligence is the combination of priors and data.
Let me state this conundrum as $\alpha P + \left(1 - \alpha\right) D = I$, where $\alpha$ is a weight, and $P$, $D$, and $I$ are priors, data, and intelligence, respectively.
So, her question is: what is the trade-off between data and prior.


### Russ Tedrake

Bringing a meta approach to the debate by counting successful demos as data, Russ Tedrake admits that _"if you see enough of those day in and day out, you start believing in data."_
It's a humble call to step outside our comfort zone, because solving some of the robotic challenges _"might require us discarding the models we have been building for a while and thinking differently about the new tools."_

He also stresses that _"embracing data does not mean know-nothingism."_
This ties to the early phase of a paradigm shift, being messy without the ability to grasp or hold on something.
Dealing with black-box models is not a great help in this regard.
At the end, he is optimistic that eventually _"empirical understanding of these new capabilities"_ will lead to further understanding to _"build the right simple models to help us deeply understand."_


### Frank Park

Winning at what cost?
What goes into foundation models is massive computing that consumes energy, water and, other infrastructure resources.
Frank Park mentions that the next data centre is as big as the size of an [Empire State Building](https://en.wikipedia.org/wiki/Empire_State_Building) on its side.
Furthermore, foundation models also need a large data set.
Frank Park comments by mocking the human data collection for being tedious and expensive, _"Come on, right? We cannot be doing this."_
On top of this, only generalizing to 99.x percent of the problem can have a real negative impact on the real world.
These long-tail events can be catastrophic, _e.g._, failures in autonomous self-driving cars.

To account for all of this, foundation needs to move towards model-based approaches.
Although _"learning is here to stay,"_ if we add all the necessary priors like equivariances and inductive biases, _"it's not a foundation model."_


### Ken Goldberg

[Ken Goldberg](https://en.wikipedia.org/wiki/Ken_Goldberg) is an excellent and entertaining moderator.
I just want to highlight the following conclusion of an interesting back-of-the-envelope calculation.
Extrapolating data as described in his editorial, it might take 100,000 years to gather the necessary amount of data for a foundation model in robotics.



## Mixing in My Two Cents

I also believe that we are in what [Thomas Kuhn](https://en.wikipedia.org/wiki/Thomas_Kuhn) called a "paradigm shift."
It presents a new emerging paradigm and novel perspectives to robotics.
However, such a transition is messy and chaotic.
It is also wasteful and, the outcome is uncertain and mysterious.

Safety at the planetary scale (_e.g._, energy footprint), societal scale (_e.g._, [trolley problem](https://en.wikipedia.org/wiki/Trolley_problem)), and individual scale (_e.g._, physical human-robot interaction) are affected by pushing more towards data-driven approaches.
Regarding concerns about safety raised by a question form the audience, Ken Goldberg refers to a demo, where a light-weight robot with a sharp razor in its hand shaves [Sami Haddadin](https://en.wikipedia.org/wiki/Sami_Haddadin).
No learning involved, just pure model-based approaches.
Jokingly, Ken Goldberg suggests doing a demo with a data-driven approach for next year.
That would be impressive, but I don't think we will have a data-driven version of it.
If we reach it with a data-driven approach, this data-driven approach wouldn't be called a foundation model.
Here I am vibing with Frank Park.

With a data gap as big as a 100,000 years of robot experiences, we will go nowhere.
On the other hand, 100,000 years of good old-fashioned engineering (GOFE) won't yield a better outcome. 
This approach might lead to more [epicycle](https://en.wikipedia.org/wiki/Deferent_and_epicycle) and, more and more circles are added to move on another circle.
This is epicycle trap, where we add and add more complexity without deeper insight.
Instead, we need more insights and understanding of the problem.
Again, data by its own is not sufficient and, at the time, quality data is needed to come up with novel models.
Here, I am vibing now with Aude Billard on this one.



### A Mask Revealing Moment in Scooby-Doo

It is always an interplay between data and model.
It always has been.

Funnily, an audience question asks the about synthetic data in learning models to just remind everyone that synthetic data comes from a model.
Bravo, what a wonderful trap!
Yeah, it is quite sneaky to sell a model-based approach as a data-based approach.

Again, by tapping on the vast knowledge of the world, we can include priors from geometry (_e.g._, line geometry), human motion control (_e.g._, impedance control), mechanics (_e.g._, energy-based modelling) to inform the data-based approach.
If we do that, we arrive at or get closer to a model-based approach.

Let me remind us, the scientific method starts with observation based on data.
For example, [Ziegler-Nichols method for tuning PID controllers](https://en.wikipedia.org/wiki/Ziegler%E2%80%93Nichols_method) is based on insights gained from looking at a large number of different processes.
Its origin is a data-driven approach, where the human is the optimizer and compressor, leading to a set of model-based rules.
Another example is [TRIZ](https://en.wikipedia.org/wiki/TRIZ), a systematic method to solve technical problems.
As it is developed from analyzing countless patents in literature, its origin is also a data-driven approach.

_"The point is, data is needed, but it is insufficient on its own.
The true thing that may help solve part of robotics is the model."_$-$Aude Billard

_"The solution takes a path through data."_$-$Russ Tedrake

Without data and purely relying on human ingenuity, we might end up with [Platonic solids](https://en.wikipedia.org/wiki/Platonic_solid) and [string theory](https://en.wikipedia.org/wiki/Thing_theory) for robotics.
It's a hot take and somewhat exaggerated, but I hope it hits the debate's vibe.
You get the point; a model is needed, but it is insufficient on its own and needs to be tested in the real world.


### Cannot See the Forest for the Trees

Learning-based approaches are here to stay.
And, that's a good thing.
No doubt about that.

We are in the midst of a paradigm shift.
The current phase of mystery, uncertainty, wastefulness, chaos, and messiness are expected. 
It is the calm after the storm that we seek. 

Let's revisit Leslie Kaelbling's point on the trade-off between data and priors.
If we change the $I$ from intelligence to insights, it is the low value of $\alpha$ in $\alpha P + \left(1 - \alpha\right) D = I$, causing the storm.
For large data-based approaches, this $\alpha$ is almost zero shattering the beliefs of GOFE people.
For them, this value should be close to one.
I believe that a typical life cycle of a research direction starts with a low $\alpha \approx 0$ and, through iteration and updating, it gradually goes to $\alpha \approx 1$.
In other words, it starts with mystery, goes through a demystifying process, and, hopefully, becomes knowledge and understanding.

We expect that with more insights $I$, we gain a higher $\alpha$ as well as $P$ and, therefore, it reduces the amount of data $P$.
For better or worse, we increase the amount of data and demand for more.
As mentioned by Animesh Garg, the community will stay longer in this empirical phase heavily relying on data.
Undoubtedly, he's right.
I also share Russ Tedrake's call to the community, to deepen their understanding fast.
Otherwise, it might become a long run of [Richard Sutton's bitter lesson](http://www.incompleteideas.net/IncIdeas/BitterLesson.html) and, we risk staying too long in this comfort zone.

I think the one of the ore disturbing aspects is that it feels like a lot of effort and time has already passed.
Again, we are experiencing this shift right now and this demystifying process takes time.
Perhaps, most of the easy problems have already been solved, and, now, we are facing mostly hard problems?

In hindsight everything looks simple; the foundations of celestial mechanics, the foundations of calculus, the foundations of optimization, and sooner or later the foundations of robotics.



### Walking Through the Woods Without the Right Gear Is Tough

As Leslie Kaelbing points out, language is not robotics.
Many of the points do not apply to robotics.
However, all models are wrong, but some are useful. 
The same for analogies, because an analogy is just an equivalent model to another model with all its flaws and more.
Therefore, it is still useful to compare robotics to language.
(It reminds me that I still need to read "Useful Not True" by Derek Silvers. It's on my bucket list.)
Her point still remains, _"it's going to be way harder"_ (Leslie Kaelbing) even if we use different approaches as pointed out by Daniela Rus.
But how much harder can it be?

Aude Billard picked up a seemingly weird question _"how much fluid dynamics does a bird know?"_ with a surprising twist.
_"Yes, the bird has the fluid dynamics in its brain, but it is not written in mathematical equations.
And in fact, what we are never discussing is the language of the model.
How do we encode that? Is it in code? Is it in actual language?
Whatever the language is, or is it in mathematics, but yes, I stand that it has a model in its brain, whatever it looks like."_
She has a good point, even if she mixes implementation and abstraction a bit, but let's stick to abstraction.
I strongly believe that this abstraction will be written in mathematical equations, rules, functions, and so on.
The language is maths.
However, it will not be written in the mathematics we know today.

They're phenomena in the real world which cannot be mathematical modeled, yet.
For instead, complexity and emergence are frontiers in physics and, physicists complain about the lack of mathematics in this frontier.
However, sometimes it looks super complicated, but it is simple. 
For example, the motion and coordination of a flock of birds or a school of fish turns out to be [surprisingly simple](https://en.wikipedia.org/wiki/Boids).
Nevertheless, without the right mathematical tool, phenomena like [Zeno's paradoxes of motion](https://en.wikipedia.org/wiki/Zeno%27s_paradoxes) or [Ehrenfest paradox of rotating a rigid disks](https://en.wikipedia.org/wiki/Ehrenfest_paradox) seem unsolvable.
The first one led to the idea of calculus, and the second one popularized tensor calculus (in a quite convoluted way, but you can connect the dots).
So, are our maths tools there yet?

Perhaps, it is time to look into those old pure mathematics write-ups?
It's like going to Göttingen in Germany to read Gauss's unpublished notebooks and hope for serendipity.
Mathematicians used to do it, even if not all mathematics maps onto physics and the real world.
Maybe it is time to look into contemporary obscure pure mathematics?


## Interesting Reads

Amato, Hutchinson, Garg, Billard, Rus, Tedrake, Park, and Goldberg
(2025).
*"Data will solve robotics and automation: True of false?": A debate*
Science Robotics; 10 (105)
[doi: 10.1126/scirobotics.aea7897](https://doi.org/10.1126/scirobotics.aea7897)

Goldberg
(2025).
*Good old-fashioned engineering can close the 100,000-year "data gap" in robotics*
Science Robotics; 10 (105)
[doi: 10.1126/scirobotics.aea7390](https://doi.org/10.1126/scirobotics.aea7390)

Clement, Peretroukhin, Giamou, Leonard, Kress-Gazit, How, Milford, Brock, Gariepy, Schoellig, Roy, Siegel, Righetti, Billard, and Kelly
*Where Do We Go From Here? Debates on the  Future of Robotics Research at ICRA 2019*
IEEE Robotics & Automation Magazine; 10 (3)
[doi: 10.1109/MRA.2019.2926934](https://doi.org/10.1109/MRA.2019.2926934)
