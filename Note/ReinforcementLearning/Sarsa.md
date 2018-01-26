# Sarsa
> Jan 17-, 2018


## [Algorithm :](#)
![Sarsa](./img/Sarsa.png) \

the basic Sarsa algorithm, there're two Loop in the algorithm. Outer one is for games(episode), and inner one is for state and actions (steps in a game). \

1. Initialize **Q-Table** (basically, set all reward = 0.0)
2. Loop setting for each game (episode) :
3. Initialize **state** in the begining of each games
4. Choose a action according to **state**
5. Loop setting for each steps
6. According to state *s* in each step, pick the Action *a* with highest reward (greedy method)
	- **ε-greedy**(Epsilon greedy) : A reward choosing policy. *ε* is a rate value. If *ε* = 0.9, its means Agent will choose maximum reward action by 90%, and 10% choose randomly.
	- Also, you can take other policy to pick reward
6. Take action *a* and then observe the environment feedback ( reward *r'* and next step state *s'* )
7. Choose next action *a* according to next state *s*
8. **Update Q-Table's reward you picked** : 
	- alpha *α* : learning-rate
	- gamma *γ* : decay-rate
	- Q(*s'*,*a'*) means : derive the according to next action *a'* and state *s'*
9. update state *s* to *s'*, action *a* to *a'* (Note that, *a'* will be next step's action.)


## [Compare to Q-Learning :](#)
As same as Q-Learning, there're two two loop in the algorithm, and **take action** before updateing the Q-Table. \
The difference between Q-Learning and Sarsa is, **Sarsa's current action was choosed in last step**, and Sarsa doesn't choose max reward action, instead, it choose conservative one. \

- Same decision method (using table to store reward), but different update method to **Q-Learning**
- Its call **on-policy**, and Q-Learning calls **off-policy**. The difference between two policy is "whether it can learn from record or not".
- Sarsa is more conservative in process.
- Sarsa actually choose action which we estimated in last stage.

# Sarsa lambda :



## Reference :
1. (video) Morvan's Sarsa tutorial in chinese ([link](https://morvanzhou.github.io/tutorials/machine-learning/reinforcement-learning/2-2-tabular-q1/))
2. (wiki) Markov decision process (MDP) ([link](https://en.wikipedia.org/wiki/Markov_decision_process))
3. (wiki) State–action–reward–state–action (Sarsa) ()