# Q-Learning
> Dec 16-23, 2017

## Concept
1. **Q-table** store values for each step and action

| step          | action1       | action2   |
| ------------- |:-------------:| :--------:|
| **step1.**    | reward1		|reward2	|
| **step2.**    | reward3       |reward4    |
| **step3.**    | reward5       |reward6    |

2. At begining of each step, choose action which has **highest reward** in this step
3. After choosing the action , you'll get real **feedback(reward) from environment**
4. Accroding to this feedback and current step, **update Q-table value** (which choosed at **step2**)
5. the main process will play this game several times
6. In each game, you will take actions and update Q-table several times, until you Win or Fail(Optional)
7. Q-Table will be preserved in the end of each game, you can also think Q-Talbe as **global variable** in the main process, so it wont be initialized in the begining of each game.

## Reference
1. Morvan's Q-Learning tutorial in chinese ([link](https://morvanzhou.github.io/tutorials/machine-learning/reinforcement-learning/2-2-tabular-q1/))