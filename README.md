# Self-Balancing-Robot-Pybullet-Simualtion

## Description

this is a followup project for the [crawlingRobot](https://github.com/omarelsayeed/Crawling-Robot-Simulation) 
- My motivation was to increase my understanding of how to approach a problem like this , how to formalize the mdp and solve it.
- also during the training tuning the agent abused bugs in the environment where it could do switches that made him jump which is unrealistic and that was really cool to see agent finding bugs in the environment !


https://user-images.githubusercontent.com/64399795/176074202-d1ae70d9-baf2-4bb1-b606-f4becf25651f.mp4



## How To Run ?

the framework can be embedded in a gym environment and you can run over it the built in DQN agents ,
For training converting to p.DIRECT will speed up the training 10x times , then you can switch it back to GUI and run agent.test().

## Relative Q-Learn 
States : our states is the pitch in the x-axis , we want to keep it at a +-0.05 where the robot is balancing , discretized to 6 states in the interval of 0.05.
![2-Figure1-1](https://user-images.githubusercontent.com/64399795/176072487-090f2c43-f500-490c-8834-4ac79b67d290.png)

Actions : the actions are 11 Velocities to switch from and to to maintain the balance.

Reward : for every state we take the cumulative sum of the rewards "hence the relative part" , and if the robot fell we give it -1000 and restart .

## Training

https://user-images.githubusercontent.com/64399795/176074552-865dcc8d-17e7-4d01-b722-aa8685236f00.mp4

## Testing 


https://user-images.githubusercontent.com/64399795/176076175-71899c1c-df9b-47ee-9533-f10392daf3ce.mp4

# Results 
The agent took like 400k steps before finding the best policy then it consistently got the reward increasing by balancing.
![image](https://user-images.githubusercontent.com/64399795/176076339-d99b01af-a68c-4b49-9f3a-194a05061a61.png)



# References 
[Pybullet Documentation](https://docs.google.com/document/d/10sXEhzFRSnvFcl3XxNGhnD4N2SedqwdAvK3dsihxVUA/edit#)

[Pybullet Tutorial](https://www.youtube.com/watch?v=kZxPaGdoSJY&t=828s&ab_channel=DanielEid)

[Stanford Reinforcement Learning Lecture 1](https://www.youtube.com/watch?v=9g32v7bK3Co&t=3866s&ab_channel=StanfordOnline)

[Stanford Reinforcement Learning Lecture 2](https://www.youtube.com/watch?v=HpaHTfY52RQ&t=3989s&ab_channel=StanfordOnline)
