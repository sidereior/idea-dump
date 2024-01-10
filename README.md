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
