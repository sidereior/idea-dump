## wot strategy explorer

This is a project I am currently planning different approaches in which to imagine a solution. The aim of the project is this: develop a tool that is able to determine an optimal strategy in which for your tank to move in the video game world of tanks given the current map. It will not consider vehicle orientation, only position at this moment. 

# Aspects
 - data exporter: in order to get the data that will be used in which to train a CNN, we will need a lot of data from games themselves. I am not very familiar with wot replay files and exporting data from them, or using some api which is able to read data. this is the first aspect in order to explore how to get reliable map data from games (ideally without the need of being in the game itself) and getting them from wotreplays or something else.

 - convolutional neural network: the approach to this should be similar to the approach outlined in cs89.31. what I am currently imagining is a way in which to add on another layer of image data that represents both vehicle information and position. initially this will look quite simple. in addition to having the traditionally 3d cnn which contains image x, image y, and rgb values, we also want to include some data such as vehicle location, vehicle hit points, vehicle type, as well as vehicle specifications. 

# More on the Convolutional Neural Network

 - I imagine an approach which simply uses image data will function, albiet pretty poorly. I'll likely start with something as simple as this, but without much data about vehicle movement I do not believe it will work well.
 - vehicle destruction will be harder than expected to make function properly. i do not want a result where vehicles which have 0 health points impact (really at all) the output of the model.
 - designing a custom neural network will be challenging. I need to figure out an angle in which to approach higher dimensionality cnns as I only have experience in working with 3d cnns for image classification. 
 - absensce of an image entirely. in the ideal solution, an image might not be needed to be passed in at all. if vehicle position data can be entered based upon the coordinate vehicle information that is extracted from replay clips.
 - different maps
 - using a pre-trained network? This may be more confusing as I try to create something which is able to accomplish the goal of the project. imagining my own approach to convolution and pooling would be entirely new to me, but if I had unlimited time I would undoubtedly do this. In this case, I think zero padding could be terrible for the quality of the model as sometimes the most important features of the map are on its edges. The only benefit the nature of this project has is that I already know the different maps and these do not change, so a lot of image data is hard-coded. right now, i'll create something working with efficientnetb7 if this is how I choose to approach it since i've used it before, possibly switching to NoisyNN as the noise appraoch probably is the future of CNNs and adversarial learning.  
 - map changes. maps have changed over time in wot. for the sake of simplicity right now, I think i'll want to choose replays over the past year to mitigate these map changes as much as possible and keep the most up-to-date playstyle. 

# More on data extraction
 - i imagine data extraction will be much more challenging than initially thought. getting an amount of data that is sufficient for training of the cnn will be challenging.  
 - which replays to choose? this is not an easy question at all to answer and is probably the most important one of the entire project, and also the one with the least verifiable evidence per time. basically, i'll just have to choose what i think is best (highest damange matches, MOE matches, etc.). one immediate problem i see is that the most useful strategy is often not the best for MOE. so, I'll need to be careful because your model is only as good and as bad as your data. for now, this problem can probably be deferred until i've got an acceptable version of the model wokring, but later this will become the question. 





# DartBored

## Simply, it's a digital whiteboard that acts similar to a permanent Instagram Story.
TLDR: The need: A lot of groups (clubs, Greek life, etc.) use different means of communication (GroupMe, Email, Slack, Text) that, for a student, is often cumbersome and annoying to manage, specially for mixing social contexts with school contexts.


- The idea began over a discussion of how there isn't a good way to facilitate a "one-way discussion". By "one-way discussion", we mean that it isn't a message feed where there are two parties communicating with each other, but rather some sort of message where a user relays information to a group (i.e. think about how most clubs at colleges go about communication--they set up a GroupMe or Slack and one or two people who are high-up in the club send meeting/event times, and everyone in the group likes the message. The conversation is one-way because a large percent of the users simply like messages and do not send messages themselves).
- We realized that a lot of people have whiteboards on their door and use these to have a one-way conversation with any passerby about any myriad of things from Minecraft Servers to graffiti to dorm parties. The whiteboard that a lot of people may have on the outside of their dorm room is unique in that a passerby may or may not be able to edit the whiteboard if they have a marker or eraser and that the whiteboard is designed for an explicitly social purpose.

## From this initial discussion I thought about the idea more and developed it into one that could be a new app that I dubbed "DartBored" (a play on Dartmouth, Whiteboard, and Bored) which would allow for groups to create digital whiteboards. There are two fundamental aspects of DartBored:
- First, the creation of boards themselves.  A board would need at least two people and could be public or private, so that anyone from two people in a dorm to an entire fraternity could create a board and convey information. At Dartmouth it is tradition for most events (club meetings, parties, etc.)  to create posters that are emailed to the entire school, so this would also address the problem of email inbox cluttering that is frequently discussed on Dartmouth's Fizz. You could also have a private board that would require some code in order for a user to join, but once joined, the user could see all activity on the digital whiteboard. The digital whiteboard itself would allow for image sharing, drawing, text editing, etc. This would also be a centralized place that you could know who is a part of each public club/group. For private boards, the board admin could configure whether or not to display members, and if a dorm room wanted to restrict some information about a get-together with just a few friends, for example, they could do so.
- Second, DartBored would also support board interaction. Once a user joins a board, they would be able to see members of this board and interact with them. For public boards such as a club, for example, a user could send a "dart" (like throwing a dart on a dartboard with an animation like such) that would be similar to how "poking" worked in the early days of Facebook and would allow for a user to anonymously send a message to this person.  In addition to throwing darts at boards, users could also interact with the boards themselves if the board admin configures this to support anyone to draw/edit the board itself. Furthermore, the board admin could also send a dart to every user who is a part of the board to notify them of changes on the board for an event or other communication.

