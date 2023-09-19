[//]: # (Image References)

[image1]: resources/640px-Udacity_logo.svg.png
[image2]: resources/reacher.gif
[image3]: resources/config.png
[image4]: resources/training.png


### ![image1]
### Deep Reinforcement Learning Nanodegree
### Policy-Based Methods | Project: *Continuous Control*
### Author : Alberto García García

#

#### Introduction


The problem to be solved in this project consists in training a reinforcement learning
agent controlling a double-jointed robotic arm. The robotic arm must reach a target location
and stay within it, obtaining a positive reward of +0.1 for every step maintaining its position in
the target location.

![image2]

The state space consists of 33 variables including information like the
velocity or the rotation of the arm among others, while the action space consists of 4 variables
representing the torque applicable to the arm joints. The problem is considered to be solved when the agent’s average score of the last
100 episodes is equal or greater than 30 points.

#### Guidelines

The whole training of the agent is implemented in the [ContinuosControl.ipynb notebook](solution/ContinuousControl.ipynb). You can either visualize the last
execution or run it by yourself in a Jupyter server. To do so, you can take the following steps to fulfill the requirements:

1. Create (and activate) a new environment with Python 3.6.

   - Linux or Mac: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- Windows: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```

2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of 
OpenAI gym.
3. Install the dependencies in the `python/` folder.
   ```bash
   cd ./python/
   pip install .
   ```
4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd`
environment.  
   ```bash
   python -m ipykernel install --user --name drlnd --display-name "drlnd"
   ```
5. Download the Unity Environment and unzip it inside the `solution/` directory. If you are using Windows 64 bits, you can skip this step since the repository already contains the environment files. Otherwise, delete the environment files and place the ones matching your OS.
	- [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
	- [Mac OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
	- [Windows (32-bits)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
	- [Windows (64 bits)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)   
6. Before running the notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

   ![image3]


#### Results

The agent is able to solve the problem in 68 episodes (averaging 30 points from episode 68 to episode 168). The weights of the actor network are stored in 
[actor.pth](solution/actor.pth) and the weights of the critic network are stored in 
[critic.pth](solution/actor.pth). Here's the agent's score history:

![image4]
