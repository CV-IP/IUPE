# Imitating Unknown Policies via Exploration (IUPE)
Official Pytorch implementation of Imitating Unknown Policies via Exploration

---

Behavioral cloning is an imitation learning technique that teaches an agent how to behave through expert demonstrations.
Recent approaches use self-supervision of fully-observable unlabeled snapshots of the states to decode state-pairs into actions.
However, the iterative learning scheme from these techniques are prone to getting stuck into bad local minima.
We address these limitations incorporating a two-phase model into the original framework, which learns from unlabeled observations via exploration, substantially improving traditional behavioral cloning by exploiting (i) a sampling mechanism to prevent bad local minima, (ii) a sampling mechanism to improve exploration, and (iii) self-attention modules to capture global features.

## Downloading the data
You can download the data we used to train our models [here](https://drive.google.com/file/d/1_wnrfv1OEM_EuPaF5tMF2l2ZJjr9lJVh/view?usp=sharing)

## Training IUPE

After downloading the expert demonstration, you can then train ABCO. There are several training scripts in the directory. 

```
./scripts/iupe_3  # Maze 3x3
./scripts/iupe_5  # Maze 5x5
./scripts/iupe_10  # Maze 10x10
./scripts/iupe_acrobot  # Acrobot
./scripts/iupe_cartpole  # Cartpole
./scripts/iupe_mountaincar  # Mountaincar
```
**We ran IUPE on a server, if you are running locally you might want to remove** ```xvfb-run -a -s "-screen 0 1400x900x24"``` **from the scripts**

## Citation

```
```