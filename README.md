## Irrigation Optimization with a Deep Reinforcement Learning model - Case study on a site in Portugal
 we trained a deep Q(LSTM)-Networks network model that uses histirocal cliamte data, soil moisture and evapotranspiration, and simply tells farmers when and how much 
 to irrigate to achieve the best productivity without wasting water for a tomato field. 

## Framework 
First, historical data are collected from various sources and prepared for use as input to the models. Then, two LSTM models are trained on the obtained historical
data to predict soil moisture for the next day and tomato yield at the end of a season, respectivly.
 Training the LSTM models is a unique process and after training, they use as a feature in the DRL training environment,
 which takes the current state $s$ (historical climate data) and action $a$ (amount of irrigation), and then returns the next state $s'$ and reward
 $r$. During the agent's training, it selects an action for the next irrigation based on the current state of the field 
 and evaluates that action using a function called $Q$-value. The environment receives the current state and the action chosen by the
 agent and indicates the next state and the reward. This interaction between the DRL agent and training environment
 is repeated until the DRL agent converges to an optimal strategy for choosing the next day's irrigation amount.
 
 ## Installation
The model depends on the following Python packages:

numpy 

tensorflow 

sklearn 

pandas 

matplotlib

For more information about the version see requirement.txt

## About the Model

choos_action:  Number of actions that agent can selected from them
Agent:  Contains the class of DQN agent and training the model.
environment: A class that define the environment of the agent.
test: test the trained agent on the test set.
train: training the agent

## Citation
@article{alibabaei2022,
title = {Irrigation optimization with a deep reinforcement learning model: Case study on a site in Portugal},
journal = {Agricultural Water Management},
volume = {263},
pages = {107480},
year = {2022},
issn = {0378-3774},
url = {https://www.sciencedirect.com/science/article/pii/S0378377422000270},
author = {Khadijeh Alibabaei and Pedro D. Gaspar and Eduardo Assunção and Saeid Alirezazadeh and Tânia M. Lima},
}
