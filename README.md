[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Kernel"

# Navigation

![Trained Agent][image1]

## Objectives

For this project, an agent need to be trained to navigate in a large, square world and collect bananas.  

## Environment Overview

**State Space**: The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  

**Action Space**: Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

**Reward**: A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

**Problem Solved**: The task is episodic. The environment is considered solved when the agent get an average score of +13 over 100 consecutive episodes.

## Instructions
### STEP 0: set up dependencies 

To set up your python environment to run the code in this repository, follow the [Udacity DRL repo](https://github.com/udacity/deep-reinforcement-learning/blob/master/README.md) instructions below.

A. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
	
B. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
C. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

D. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

E. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

![Kernel][image2]


### STEP 1: Clone Repository

Open up a terminal, go to the directory of your choice and clone the repository

```
git clone https://github.com/wjlgatech/DRL-dqn-navigation.git .
```

### STEP 2: Download Environment

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the same folder as the downloaded repository, and unzip (or decompress) the file. 

### STEP 3: Run Codes

One way is that you open the Navigation.ipynb notebook to follow instructions there:

```
jupyter notebook Navigation.ipynb
```


Another way is that you train the agents with

```
python train.py
```

and test the trained agents with
```
python test.py
```

## Code Overview

The code consists of the following modules

```
Navigation.ipynb - the main notebook
dqn_agent.py - defines the Agent that is to be trained
checkpoint.pth - is the final trained dqn network
train.py - train the dqn agent
test.py - test the performance of the trained agent
Navigation_Report.ipynb - the project report
```

## Results

DNQ is able to solve the environment in 2866 episodes with average Score: 13.05

