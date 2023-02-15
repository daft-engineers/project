# Daft Engineers Vocoder Project

# Scrum notes

## 20/01/2023
2 main project ideas:
Gimbal: Good pitch/marketing potential as a unspillable beer carrier thing. Plenty of real time processing to be done with some filtering and control. Mechanical parts could be diifficult to create and servo motors of suffiient performance are expensive, and would require us to spend our owm money on it. Would have to be battery powered which adds to cost and complexity that isn't really contributing to the mark. The complex processing is a double edged sword as if it isn't close to perfect then it'll be completely useless.
Vocoder: Good to show off as a final product, but possibly a poorer initial pitch idea. Real time audio processing with lots of filters. Electronics are simple enough and it would generally need very little we don't have already. Producing the carrier with the hyasynth is cool as it modifying our own keyboard into a midi controller for it and having the pi produce the carrier. It's possibly a simpler project, but there's plenty of augmentations you can make to flesh it out. 
Also considered: Slit scan camera, but this was retired as it is probaby better as a post processing method.

Vocoder was chosen as it was what we kept coming back to.
A Github project was created and fleshed out with a few initial issues, Mark was given the task of doing a little investigation and making sure a vooder was reasonable with the time we had to create it and the processing power available. 

Minimum viable product would be to take voice as one input and the carrier as the other, do the processing in real time and produce an output. 
Improved experience would be to have a physical keyboard as well and have the pi create the carrier using the input from the keyboard. 

## 23/01/2023
Mark had a look and decided that the vocoder was reasonable. Mark plans to put together a proof of concept in ableton.
Matthew plans to make the presentation and look at the licence stuff
Angus plans to make the presentation and have a look at the hardware plan.
James plans to make the presentation and take a look at a software overview. 

#15/02/2023
Matthew has been looking at linting and static analysis and integrating them with cmake. He will finish that off and maybe start writing code.
Mark has started working with googletest, started writing the filter class and started work on the logo. mark will continue with those, prioritising the unit tests. 
Angus will start working on the CI.
James has had a look at doxygen, linting and testing framework and sourced the codec zero hardware and will try to finish doxygen and startloooking at the audio driver. 

