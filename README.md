# DonkeyCarML
  In this project, I trained a [neural net](https://github.com/JohnPalevich/DonkeyCarML/blob/master/models/mypilot.h5) using supervised learning to predict the steering and throttle given a picture of the track.
# How to Download
  To download the necessary tools, I followed the instructions from the DonkeyCar virtual race league [here](https://docs.donkeycar.com/guide/simulator/) 
# Problems I Ran Into
  An annoying error I ran into while trying to set the project up was Miniconda required the install location to have no spaces. However, my users folder name was "John Palevich" and I didn't have the permissions to change the folder name. To get around this, I created a new user on my pc with a name that did not contain a space. <p>
  A secondary problem I ran into was that my CPU is very weak, so the simulation ran on my computer at around 4 frames per second. To cope with this, I borrowed a friends computer to host the simulation, and I connected to it using the internet. Here, the simulation ran at a more bearable 17 fps. Fortunately, I have a strong GPU, so after I collected the training data, training the neural net was fairly quick.

# How I Trained
  I trained using supervised learning. I manually drove the simulated donkey car around the track 10 times. During the 10 times a script recorded images of the screen as well as position, throttle and angle every 20th of a second. From this, a training algorithm trained the neural net using the [data set](https://github.com/JohnPalevich/DonkeyCarML/tree/master/data/tub_1_20-05-04) I created.

# Results
  Below is a graph generated to show how the bot became more accurate as the training algorithm repeated the learning on the training set: <p>
![Figure_1](https://user-images.githubusercontent.com/22034172/81135882-b0fe6e80-8f0e-11ea-9470-2abfccb8df11.png)
<p>
  In addition, I have attatched a side by side comparison video of a trained car and myself driving around the track. <p>
<a href="http://www.youtube.com/watch?feature=player_embedded&v=Z4yH-NK1KHg
" target="_blank"><img src="http://img.youtube.com/vi/Z4yH-NK1KHg/0.jpg" 
alt="SideBySideComparison" width="960" height="720" border="10" /></a>
  
# Plans for the Future
  In the future, I plan on joining the DonkeyCar virtual racing league. To do so though, I plan on further training my neural net so that it can compete at a higher level. Currently, it is taking a slow but steady approach, only ever maxing its speed out at 30% of the maximum throttle. <p>
   In addition, the neural net is trained only to go forward. To improve its capabilities, say if it got knocked off course by another car, I plan to train it by randomly spawning the car at a specific x and z coordinate. Here, using reinforcement learning, it will learn how to straighten itself back on course.
