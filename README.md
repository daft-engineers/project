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

# 15/02/2023

Matthew has been looking at linting and static analysis and integrating them with cmake. He will finish that off and maybe start writing code.

Mark has started working with googletest, started writing the filter class and started work on the logo. mark will continue with those, prioritising the unit tests. 

Angus will start working on the CI.

James has had a look at doxygen, linting and testing framework and sourced the codec zero hardware and will try to finish doxygen and startloooking at the audio driver. 

# 16/02/2023

James: looked at alsa, may be worth considering jack or pulse if they're easier to use. Will keep looking at the audio driver stuff. 

Mark: set up google test with cmake, made it work with the newest version of gtest. Made 2 draft logos, with the second one being better recieved. Will finalise logo, and addd to accounts. Do more filter code, probaby start with unit tests.

Matthew: Set up clang format and clang tidy, with definitions. Wrote a script that runs them both. Will finish the work on clang format and tidy related CI and then pick up another ticket, probably audio driver. 

Angus: Had a look at building and running tests within CI. Will continue with CI work

Clang format: committed files should pass clang format, can block merge until they work.

# 22/02/2023

Angus: Got CI working to build and run the googletests, as well as the static analysis and formatting tools. Will need a little change and it will be ready to review. 

James: Decided we're best using jack rather than straight alsa. Had a look at getting a callback running with that. Will keep working on that, hopefully with some help. 

Mark: Got the logo just right, and attached it to all of our accounts. Got our first subscriber on our youtube account. Had a look at filters, made a little progress on unit testing. Will keep looking at the unit tests and try and get a filter class going. 

Matthew: Previously completed the linting standard ticket, wrote a readme that gives an intro and includes build info. May start looking at data flow, or another ticket from backlog. 

Dependencies, need to look at the "best" way to get them included. Made a ticket for it. 

# 23/02/2023

Matthew: Made sequence diagram, attached it to the issue and put it in the readme, and added the ticktok account to the readme. This finished the data flow ticket. Going to pick up a programming ticket. Going to update checks.sh to work on header files. 

Angus: Broke CI worse, but has a plan to fix it. Will fix it today. 

Mark: Made the audio class with all the subclasses to represent messages. Did a little work on the filter class, all the setup is don. Will continue that today. Will probably start by getting unit tests running and failing for the filter class. 

James: Looked at audio in. Will try and get jack registering call backs and translating them to the audio class. 

Audio class: Had a discussion about the audio class. James felt that there was no value to having different types depending on where the audio came from, and that it made the system more complicated and less modular. Matthew felt that this was making good use of the type system as we probably won't be mixing and matching the order of operations. We decided to simplify, and move one of the subclasses out as it wasn't actually audio.

# 01/03/2023

Matthew: Worked on audio driver, discovered that the zodec zero doesn't apper to be working. Alsa was not able to find it. Reinstalled pios with a gui. Made it appear to the os but still couldn't get it working. Installed more alsa stuff and pulse. Different configs give different errors. Auidio works fine through the hdmi. Tried a new PI. Will head into the lab to ask tom ohara about it. 

James: did a bit of work to checks.sh to add header file checking, which meant moving the headers and some other related stuff. Will finish getting the checks stuff reviewed and merged and pick up something or take another loook at doxy.

Mark: Wrote the unit tests, and then realised that a delay needs to be added as the IIR filter can't start outputting immidiately. Will continue work on that. 

Angus: Got CI finished, and picked up the level control module ticket. Will continue work on that. 

