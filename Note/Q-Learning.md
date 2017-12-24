# Q-Learning
> Dec 16-23, 2017

## Concept
1. **Q-table** store values for each step and action \

| step          | action1       | action2   |
| ------------- |:-------------:| :--------:|
| **step1.**    | reward		|reward		|
| **step2.**    | reward        |reward     |
| **step3.**    | reward        |reward     |

\
2. At begining of each step, choose highest reward action
3. After choosing a answer , we'll get real feedback form env.
4. Accroding to this feedback and step, update Q-table value (which choosed at **step2**)
5. the main process will play this game several times
6. In each game, you will take actions and update Q-learning several times, until you Win or Fail(Optional)
7. Q-Table will be preserved in the end of each game, you can also think Q-Talbe as **global variable** in the main process, so it wont be initialized in the begining of each game.

