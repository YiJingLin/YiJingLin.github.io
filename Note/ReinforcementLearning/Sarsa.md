# Sarsa
> Jan 17, 2018

## [Concept :](#)
- store **rewards** in **Sarsa Table**


## [Algorithm :](#)


## [Compare to Q-Learning :](#)
- Same decision method (using table to store reward), but different update method to **Q-Learning**
- Its call **on-policy**, and Q-Learning calls **off-policy**. The difference between two policy is "whether is can learn from other record or not". 
- Sarsa is more conservative in the training process.
- Sarsa actually choose action which we estimated in last stage.

# Sarsa lambda :


## Reference :
1. (video) Morvan's Sarsa tutorial in chinese ([link](https://morvanzhou.github.io/tutorials/machine-learning/reinforcement-learning/2-2-tabular-q1/))
2. (wiki) Markov decision process (MDP) ([link](https://en.wikipedia.org/wiki/Markov_decision_process))
3. (wiki) State–action–reward–state–action (Sarsa) ()