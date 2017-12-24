# Q-Learning
> Dec 16-23, 2017

## Concept
- **Q-table** store values for each status and action

| status        | action1       | action2   |
| ------------- |:-------------:| :--------:|
| **status1.**  | reward1		|reward2	|
| **status2.**  | reward3       |reward4    |
| **status3.**  | reward5       |reward6    |

- At begining of each status, choose action which has **highest reward** in this status
- After choosing the action , you'll get **reward and next status from environment**
- Accroding to this feedback and current status, **update Q-table value** (which choosed at **status2**)
- the main process will play this game several times
- In each game, you will take actions and update Q-table several times, until you Win or Fail(Optional)
- Q-Table will be preserved in the end of each game, you can also think Q-Talbe as **global variable** in the main process, so it wont be initialized in the begining of each game.

## Algorithm
![algorithm](./source/Q-learning/QLearning_algo.png) \
the basic Q-learning algorithm.There's two Loop in the algorithm, outer one is for games, and inner one is for each status and actions (in a game). \
1. 

## Reference
1. (video) Morvan's Q-Learning tutorial in chinese ([link](https://morvanzhou.github.io/tutorials/machine-learning/reinforcement-learning/2-2-tabular-q1/))
2. (video) How Q-table updates ([link](https://www.youtube.com/watch?time_continue=207&v=qz_4kDieX64))