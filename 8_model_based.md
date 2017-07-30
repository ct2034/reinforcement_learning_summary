<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Model Based Reinforcement Learning
* auto-gen TOC:
{:toc}

## Intro
* pros:
    - Can efficiently learn model by supervised learning methods
    - Rapid adaptation to new problems and situations (via planning)
    - Can reason about model uncertainty

* cons:
    - Disadvantages: two sources of approximation error!
    - In estimating model and value function
    - If model is inaccurate ⇒ planning will compute a suboptimal policy
    - Hence, asymptotically model-free methods are often better
    - *Solution* 1: reason explicitly about model uncertainty (BRL)
    - *Solution* 2: use model-free RL when model is wrong
    - *Solution* 3: integrated model-based and model-free

* Learning allows an agent to improve its policy from its interactions with the environment.
* Planning: to improve its policy w/o further interaction.


## FlatMC
![](https://farm5.staticflickr.com/4309/35878109330_b66c0d9ea6_z_d.jpg)

## MCTS
![](https://farm5.staticflickr.com/4294/36139063821_52bb23af15_z_d.jpg)
![](https://farm5.staticflickr.com/4314/36139064531_cba29c0065_z_d.jpg)

## TD-search
* While MCTS applies MC control to sub-MDP from now,
* TD search applied SARSA.
* For each sim step:
Update the Q values using (s, a, r, s', a')

* model-free
* bootstraping

## Explore / Exploit Strategies
* RL agents start to act without a model of the environment: have to learn from its experience what to do in order to fulfil tasks and achieve high average return.
* Online decision-making involves a fundamental choice:
    - Exploitation: Make the best decision given current information
    - Exploration: Gather more information
* The best long-term strategy may involve short-term sacrifices
* Gather enough information to make the best overall decisions ⇒ exploration as fundamental intelligent behaviour
