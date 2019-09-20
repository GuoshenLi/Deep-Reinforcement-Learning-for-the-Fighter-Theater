# Deep-Reinforcement-Learning-for-the-Fighter-Theater

## Overviews

* Inspired by intelligent gaming, I focus on how to use Deep Reinforcement Learning algorithm to play the Fighter Teather in which heroes of both sides can fight against those in the opposite and seek energy stones.

* The whole project contains 2 parts. Using python to build a game and training the game with Deep Reinforcement Learning.


## Installation Dependencies
* pytmx 3.21.5
* pygame 1.9.3
* psutil 5.4.3
* Python 2.7
* OpenCV-Python
* TensorFlow 1.10.1 (make sure to install TensorFlow that corresponds to Python 2.7!)

## Some Suggestions about the Installation Dependencies (Important!) 

* Since the game code is written in Python 2.7, make sure that you use Python 2 instead Python 3 to run.
* For Windows users, I have already read some files that mention Tensorflow does not have the corresponding version to Python  2.7 under Windows system. So, I recommend you use Mac or Linux to run the code. 

* I run my code on Mac, so if you have any problem in doing so, feel free to contact me.



## How to train the network?
* **Unzip the zip file Fighter_DQN_2015Nature.zip or Fighter_Double_DQN first**

* Train the network with the following parameters **Do not import any saved networks!!**
```
OBSERVE = 100000. # timesteps to observe before training
EXPLORE = 1000000. # frames over which to anneal epsilon
FINAL_EPSILON = 0.0001 # final value of epsilon which is 0.0001
INITIAL_EPSILON = 1 # starting value of epsilon which is 1
```

* Use the following command!
```
cd Fighter
python game
```

* **After 2000000 iterations, it will automatically show two diagrams of the Average Reward and the Max Q_value history, and it will also store the relative data the two diagrams into mat file to reuse it later.**

* **The Average Reward of one game epoch equals to total reward of the game epoch divided by total time step of that epoch!!**

## Future Work
**I will update some details about the code and make some adjustments to optimize it if I have time.**

* I have already uploaded the 2015 Nature DQN and Double DQN for training, **the 2013 NIPS DQN will be uploaded later!**
* Ideas2: Utilizing Duelling DQN or prioritized experience replay to see how it can improve the performance of DQNs.

**But it all depends on time!!!**

## Update Logs
2019.9.20 China


## Warnings
* I am GuoshenLi, and I hope you can respect my hard work during the entire summer vacation. Any **plagiarism** is not allowed. But I am looking forward to **cooperating** with someone who is also interested in reinforcement learning. 

## Acknowledgement
Special thanks to **Dr.Zhang** who gave me inspiration of the project! 

## Reference & Disclaimer

* The game code is inspired by https://github.com/lfkdsk/FighterTheater and I made some changes of the game to make it less chaotic.
* The DQN code is based on https://github.com/yenchenlin/DeepLearningFlappyBird
