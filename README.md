# How to approach this Readme?
 - I ask that if you want to work on any of these ideas that you reach out to me @ alexander.l.nanda.27@darmouth.edu . I'd be down to talk about them and am curious about innovative approaches to solving problems that you may have. 
 - Ideas in this .md file are listed one after another. You may have to do a bit of scrolling to get to an idea that you find interesting. Here is a list of all current ideas:

## gdbpilot, an extension for gdb that uses a LLM to help you debug 
## DartBored, a digital whiteboard social media app for college students. 
## World of Tanks strategy automator tool.
## AI Agent Swarm Society/Strategy Game simulator


# gdbpilot 
## an extension for gdb that uses a LLM to help you debug
[in progress]

# DartBored

## Simply, it's a digital whiteboard that acts similar to a permanent Instagram Story.
TLDR: The need: A lot of groups (clubs, Greek life, etc.) use different means of communication (GroupMe, Email, Slack, Text) that, for a student, is often cumbersome and annoying to manage, specially for mixing social contexts with school contexts.


- The idea began over a discussion of how there isn't a good way to facilitate a "one-way discussion". By "one-way discussion", we mean that it isn't a message feed where there are two parties communicating with each other, but rather some sort of message where a user relays information to a group (i.e. think about how most clubs at colleges go about communication--they set up a GroupMe or Slack and one or two people who are high-up in the club send meeting/event times, and everyone in the group likes the message. The conversation is one-way because a large percent of the users simply like messages and do not send messages themselves).
- We realized that a lot of people have whiteboards on their door and use these to have a one-way conversation with any passerby about any myriad of things from Minecraft Servers to graffiti to dorm parties. The whiteboard that a lot of people may have on the outside of their dorm room is unique in that a passerby may or may not be able to edit the whiteboard if they have a marker or eraser and that the whiteboard is designed for an explicitly social purpose.

## From this initial discussion I thought about the idea more and developed it into one that could be a new app that I dubbed "DartBored" (a play on Dartmouth, Whiteboard, and Bored) which would allow for groups to create digital whiteboards. There are two fundamental aspects of DartBored:
- First, the creation of boards themselves.  A board would need at least two people and could be public or private, so that anyone from two people in a dorm to an entire fraternity could create a board and convey information. At Dartmouth it is tradition for most events (club meetings, parties, etc.)  to create posters that are emailed to the entire school, so this would also address the problem of email inbox cluttering that is frequently discussed on Dartmouth's Fizz. You could also have a private board that would require some code in order for a user to join, but once joined, the user could see all activity on the digital whiteboard. The digital whiteboard itself would allow for image sharing, drawing, text editing, etc. This would also be a centralized place that you could know who is a part of each public club/group. For private boards, the board admin could configure whether or not to display members, and if a dorm room wanted to restrict some information about a get-together with just a few friends, for example, they could do so.
- Second, DartBored would also support board interaction. Once a user joins a board, they would be able to see members of this board and interact with them. For public boards such as a club, for example, a user could send a "dart" (like throwing a dart on a dartboard with an animation like such) that would be similar to how "poking" worked in the early days of Facebook and would allow for a user to anonymously send a message to this person.  In addition to throwing darts at boards, users could also interact with the boards themselves if the board admin configures this to support anyone to draw/edit the board itself. Furthermore, the board admin could also send a dart to every user who is a part of the board to notify them of changes on the board for an event or other communication.


# AI Agent Swarm Society/Strategy Game simulator (formerly AI wargamging tool)

## This AI wargaming tool is one which uses the power of agent swarms in order to play and simulate complex strategy games on both a micro and macro scale, such as wargaming.
Explanation:
- First, on agent swarms. The more I read about them and mess around with langchain, autogen, or HAAS to create swarms, the more I am convinced that this is how AGI will be achieved. Here's how ChatGPT explains agent swarms: "Agent swarms, also known as swarm intelligence, refer to systems where numerous agents, typically simple in terms of their individual behavior, interact to create complex, often intelligent, collective behaviors. This concept is inspired by natural phenomena such as the flocking of birds, schooling of fish, or the behavior of ants and bees. In computational terms, these agents are often represented as simple algorithms or rules. When they operate together, they can solve complex problems or simulate complex systems." Basically, in this case, agent swarms will be such that an agent represents one unit of the game being played. In a wargame, maybe one unit could be a soldier. An example prompt to our LLM could be something like "You are a soldier within X batallion at Y location currently situated with Z. You have the ability to interact with all levels of the game including your boss, your friends, hardware and software, and much more. You are a person and make informed decisions." Obviously this example is for a soldier (and as a note I don't condone or support military applications of this), but what this demonstrates is the ability to create a system that is sufficiently complex to model the way in which a society functions. Really, this idea is a glorified text-based video game where you have many many many different AI instances acting. 
- Second, a problem. From what I have explored with Agent Swarms, the biggest problem with this entire system is the fact that it is not autonomous (well, not yet). I'd give it three months from November, 2023 for there to be a sufficiently good python library for creating entirely autonomous agent swarms. What this means is that the creation (and destruction) of these agents would need to occur manually (or at least would need to be an explicitely created tool for an agent to interact with) and this means that the system can not be overly complex. I could get this to work for a single company of soldiers, but I want the actual application to function something like this. 

```
User: I want to play a strategy game where i have a fully-simulated ancient roman legion of marcus aurelius fighting the forces of the  Germanic Marcomanni in the macromanni war. simulate it for me. 
LLM: Okay! Here you go: ...

```

- I'd reccomend for you to check out some videos from Mervin Praison on the emerging field of Agent Swarms to better understand how they work, but I want the entire game and strategy to be simulated and managed entirely by the LLM without an ounce of interaction from me, and simulated down to conversations between different soldiers themselves, as well as up to movements of entire legions. 

##The best thing about this approach is that it could easily be applied to a miriad of other applications of social science (what if you had an entirely AI social media where it is just AI talking with AI?) and that LLMs are trained on historical data. As long as the LLM know about some sort of structure of a group, it could emulate it with just a handful of words.  

- How this works. [This paper](https://arxiv.org/abs/2305.11541) is the bread and butter of this entire idea. The entire reason why agent swarms are useful is because giving a smaller domain of a problem is better than a larger one (obviously), but the extent to which it improves Q&A is pretty cool. On the level of the structure of the LLM to create the simulation, I would envision it to be similar to [HAAS](https://github.com/daveshap/OpenAI_Agent_Swarm) where there is a sort of "agency board" that has the power to spawn and destroy instances, and then subsequently desigenated and oversees the creation of a system that is able to complexly model and interact with eachother.

## as a final note, the government will pay you $1M (over 2 years) to make an automated wargaming tool. [See here] (https://www.dodsbirsttr.mil/topics-app/?baa=DOD_SBIR_2024_P1_C1)



#wot strategy explorer

This is a project I am currently planning different approaches in which to imagine a solution. The aim of the project is this: develop a tool that is able to determine an optimal strategy in which for your tank to move in the video game world of tanks given the current map. It will not consider vehicle orientation, only position at this moment. 

## Aspects
 - data exporter: in order to get the data that will be used in which to train a CNN, we will need a lot of data from games themselves. I am not very familiar with wot replay files and exporting data from them, or using some api which is able to read data. this is the first aspect in order to explore how to get reliable map data from games (ideally without the need of being in the game itself) and getting them from wotreplays or something else.

 - convolutional neural network: the approach to this should be similar to the approach outlined in cs89.31. what I am currently imagining is a way in which to add on another layer of image data that represents both vehicle information and position. initially this will look quite simple. in addition to having the traditionally 3d cnn which contains image x, image y, and rgb values, we also want to include some data such as vehicle location, vehicle hit points, vehicle type, as well as vehicle specifications. 

## More on the Convolutional Neural Network

 - I imagine an approach which simply uses image data will function, albiet pretty poorly. I'll likely start with something as simple as this, but without much data about vehicle movement I do not believe it will work well.
 - vehicle destruction will be harder than expected to make function properly. i do not want a result where vehicles which have 0 health points impact (really at all) the output of the model.
 - designing a custom neural network will be challenging. I need to figure out an angle in which to approach higher dimensionality cnns as I only have experience in working with 3d cnns for image classification. 
 - absensce of an image entirely. in the ideal solution, an image might not be needed to be passed in at all. if vehicle position data can be entered based upon the coordinate vehicle information that is extracted from replay clips.
 - different maps
 - using a pre-trained network? This may be more confusing as I try to create something which is able to accomplish the goal of the project. imagining my own approach to convolution and pooling would be entirely new to me, but if I had unlimited time I would undoubtedly do this. In this case, I think zero padding could be terrible for the quality of the model as sometimes the most important features of the map are on its edges. The only benefit the nature of this project has is that I already know the different maps and these do not change, so a lot of image data is hard-coded. right now, i'll create something working with efficientnetb7 if this is how I choose to approach it since i've used it before, possibly switching to NoisyNN as the noise appraoch probably is the future of CNNs and adversarial learning.  
 - map changes. maps have changed over time in wot. for the sake of simplicity right now, I think i'll want to choose replays over the past year to mitigate these map changes as much as possible and keep the most up-to-date playstyle. 

## More on data extraction
 - i imagine data extraction will be much more challenging than initially thought. getting an amount of data that is sufficient for training of the cnn will be challenging.  
 - which replays to choose? this is not an easy question at all to answer and is probably the most important one of the entire project, and also the one with the least verifiable evidence per time. basically, i'll just have to choose what i think is best (highest damange matches, MOE matches, etc.). one immediate problem i see is that the most useful strategy is often not the best for MOE. so, I'll need to be careful because your model is only as good and as bad as your data. for now, this problem can probably be deferred until i've got an acceptable version of the model wokring, but later this will become the question. 






