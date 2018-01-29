# [pySC2](#)

PySC2 is DeepMind's Python component of the StarCraft II Learning Environment (SC2LE).

## Quick Started :

### Installation
1. First of all, install [pysc2](https://github.com/deepmind/pysc2) package

- install with git-cloned repository (recommend)

```sh
git clone git@github.com:deepmind/pysc2.git
pip install pysc2/
```

- install by **pypi**

```sh
pip install --upgrade pysc2
```

2. Then, download and install starcraft2 game software through [Battle.net](https://tw.battle.net/account/download/index.xml) .

3. Remember to download some Maps and Replays \
(Note that there're some constraints of directory structure. See details in [link](https://github.com/Blizzard/s2client-proto#downloads))

### Run
- Run default agent :

```sh
python -m pysc2.bin.agent --map Simple64
```

- Run with user control :

```sh
python -m pysc2.bin.play --map Simple64
```

- Run for Replays :

```sh
python -m pysc2.bin.replay_actions --replay <absolute path>
```

- check map list : (not work)

```sh
python -m pysc2.bin.map_list
```


## Reference :
1. (Github)deepmind/pysc2 ([link](https://github.com/deepmind/pysc2))