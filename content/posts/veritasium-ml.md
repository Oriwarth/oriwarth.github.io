---
title: "Veritasium: Human Expertise and Machine Intelligence"
date: 2022-08-26T16:17:22-06:00
draft: false
---

A few weeks ago Veritasium released a video titled [The 4 things it takes to be an expert](https://www.youtube.com/watch?v=5eW6Eagr9XA) talking about how humans leverage their cognitive abilities in order to excel at their chosen disciplines. The approach of humans take at developing expertise has many parallels to techniques used in Machine Learning today. This blog is intended to be a companion piece to his video. So go watch that first. Disclaimer: these are mostly uncooked thoughts. 

## Chess board reconstruction
After a brief introduction, the video goes through a study in which Master, A-class and novice chess players are asked to reconstruct a chess board from a real game. The participants can look at the reference image, and the best performance is achieved by looking at the reference image the lowest number of times. Unsurprisingly, the Master took fewer peeks at the reference, while the novice took the most. 

Now, when presented with a random board configuration, the participants from all three groups had to take the same number of peeks. Meaning that the master and a-class players had no advantage over the novice. This can be seen as a sort of domain-specific compression in computing science terms.

An example of this can be an autoencoder, where it takes an input and transforms it into a vector in feature-space. However, autoencoders are (mostly) only useful in the specific domain in which they have been trained. Say, if an autoencoder is trained on a facial-recognition dataset, then it will learn the feature-representation for eyes, nose, mouth, etc. However, give that same autoencoder a picture of a flower and there's no way to tell how that will be interpreted.

Further, intelligence as compression is a concept explored in the [Hutter Prize](https://en.wikipedia.org/wiki/Hutter_Prize). Specifically, since the Hutter Prize deals with text, it is lossless compression. In the case of chess-board reconstruction, it is also in the context of lossless compression. In which, again, the masters are more effective at losslessly compressing board configurations. 

Putting two and two together, there is a way in which chess players can _encode_ a board configuration much more effectively than novices. In the same way that an autoencoder would. They recognize the relationships between the pieces (semantic concepts). And, parallel to an autoencoder, they become ineffective when presented with an input in which these semantic concepts are missing -- the random configuration.

"Chessmasters don't have better memory in general, they are better at detecting patterns in the board."

He calls it _"chunking"_, but of course, _feature space_ is a better name for this concept.

## Four criteria for expertise

Presented in the video, these are:
### 1. Repeated attempts with feedback
This has an obvious parallel to supervised learning. And if we want to emphasize the **repeated** portion of this statement, then this could be translated directly into the multiple epochs in which a Neural Network is trained. 

An aside -- the subject of  pundits that are unable to make accurate predictions in fields such as global politics is explored more deeply in the book "Black Swan". Shout-out to NNT.

### 2. Valid Environment
Does this also remind you of Reinforcement Learning? If an agent has repeated experiences with feedback but the action has no effect to the feedback (observation) it receives, then there is nothing to be learned. Even in the case of the multi-armed bandits, the agent can learn each machine's _expected_ payout. The analogy used in the video is that a roulette player will not become an expert. Although, being nitpicky, he could find the optimal policy; RL agents have been applied frequently to games of chance.

That a casino is not the best analogy for a messy and random environment is the main point of the _ludic fallacy_. Second shout-out to NNT. 

Now for a Chollet point, the poor performance of investors in the stock market and how supervised ML also underperforms in these relates to the phrase "looking in the rear-view mirror is not a good way to drive", given in the book _Deep Learning with Python_. Meaning that past performance is not an indicator of future performance. Other names for this would be: poor autocorrelation or bad for autoregression. I think this is also covered in an NNT book.

### 2.1 On the side note
Veritasium describes an experiment in which the behavior of rats and humans is compared. Two buttons are presented to the participants: green and red. Green lights up 80% of the time, while red lights up the remaining 20%. Before each round (episode) the participants are asked to press the button they think will light up. If they guess correctly, then they receive a treat, else they get an electric shock. 

Rats quickly learn that the _optimal policy_ is to only press the green button, and enjoy an 80-20 split on treats vs shocks. On the other hand, humans will pick mostly the green button, but every so often, they will pick the red button. A less acute viewer than you, my dear reader, would shun humans for their poor mental abilities. However, for you and I, it is clear that humans are following an e-greedy policy. Meaning, than humans by nature have a larger tendency to explore in the explore-exploit continuum than rats do. This is a point in favor of humans by any measure.

### 3. Timely feedback
Or on the challenge of delayed rewards. This is of particular concern for human occupations such as radiologists, college admission boards and recruiters. To measure human performance, a study was conducted in college admissions where a "formula" (I guess a regression model of: _college grades_ = f(_high school grades_)) was compared against human counselors. The formula outperformed most of the counselors. Maybe this means that using a pre-trained policy can be used for delayed rewards in reinforcement learning. Certainly this falls in "Bitter Lesson" territory. Where, maybe with enough data and computation, delayed rewards cease to be a problem. It would be interesting to see the current state of the art in this sub-area.

### 4. Don't get too comfortable: Deliberate practice
To become an expert one must practice at the edge of one's current performance. This is a analogous to online learning, instead of offline. Where the agent continuously takes in new lessons instead of relying on a pre-trained policy. This is essential to deal with a changing (and challenging) world. Humans are still better than computers at this. 

## Takeaways
The parallels in human and machine intelligence run deep, and it is still not clear how closely they do. In the same way that a bird and a plane are both capable of flying, they have their similarities and their differences. They both share commonalities like two symmetric wings on a central body (fuselage), a smaller set of wings at the back for stability, and a pointy tip (beak). However, the propulsion methods are vastly different (flapping wings vs engines). The commonalities and divergences of humans and machines in matters of intelligence are still being defined. And there are many exciting developments in the years to come. What a time to be alive!

Until next time,
Oriwarth
