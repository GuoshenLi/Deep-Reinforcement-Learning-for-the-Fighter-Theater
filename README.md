# Deep-Reinforcement-Learning-for-the-Fighter-Theater

## Overviews

* Inspired by intelligent gaming, I focus on how to use Deep Reinforcement Learning algorithm to play the Fighter Teather in which heroes of both sides can fight against those in the opposite and seek energy stones.

* The whole project contains 2 parts. Using python to build a game and training the game with Deep Reinforcement Learning.

## Boom!! Super Cool! It works!
### Pre_train (here is a Gif) How Silly the Green Heroes are!
![image](https://github.com/GuoshenLi/Deep-Reinforcement-Learning-for-the-Fighter-Theater/blob/master/pre_train.gif)

### Post_train (here is also a Gif) The Green Heroes Can Win the Game by Fighting the Red Heroes!
![image](https://github.com/GuoshenLi/Deep-Reinforcement-Learning-for-the-Fighter-Theater/blob/master/post_train.gif)

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


## How to Run?
* **Unzip the zip file Fighter.zip first**
* Note: I recommend to run in the terminal and make sure you install all the dependencies before running!

```
cd Fighter
python game
```

## How to reproduce the pre and post_train Gif?
* **Unzip the zip file Fighter_DQN.zip first**

* If you want to reproduce the pre_train_model (The silly green heroes), make sure you set the parameters in the DQN_fighter file as follows and **Do not import any saved networks!!**
```
OBSERVE = 100000. # timesteps to observe before training
EXPLORE = 1000000. # frames over which to anneal epsilon
FINAL_EPSILON = 0.0001 # final value of epsilon which is 0.0001
INITIAL_EPSILON = 1 # starting value of epsilon which is 1
```
* If you want to reproduce the post_train_model (The successful green heroes), make sure you set the parameters in the DQN_fighter file as follows and **Import the saved networks!!**
```
OBSERVE = 100000. # timesteps to observe before training
EXPLORE = 1000000. # frames over which to anneal epsilon
FINAL_EPSILON = 0 
INITIAL_EPSILON = 0 
```
**Import the saved networks like this in the DQN_fighter file!!**
```
checkpoint = tf.train.get_checkpoint_state("saved_networks")
if checkpoint and checkpoint.model_checkpoint_path:
    saver.restore(sess, checkpoint.model_checkpoint_path)   
    print("Successfully loaded:", checkpoint.model_checkpoint_path)
else:
    print("Could not find old network weights")
```

## Future Work
**I will update some details about the code and make some adjustments to optimize it if I have time.**

* Ideas1: Comparing the performence of the 2 versions of DQN in 2013 NIPS and 2015 Nature (with or without fixed Q target) 
* Ideas2: Utilizing Double DQN to see how it can solve the problem of overestimation of Q value by traditional DQNs. 

**But it all depends on time!!!**

## Update Logs
2019.9.1 China
2019.8.30 China


## Warnings
* I am GuoshenLi, and I hope you can respect my hard work during the entire summer vacation. Any **plagiarism** is not allowed. But I am looking forward to **cooperating** with someone who is also interested in reinforcement learning. 

## Acknowledgement
Special thanks to **Dr.Zhang** who gave me inspiration of the project! 

## Reference & Disclaimer

* The game code is inspired by https://github.com/lfkdsk/FighterTheater and I made some changes of the game to make it less chaotic.
* The DQN code is based on https://github.com/yenchenlin/DeepLearningFlappyBird
