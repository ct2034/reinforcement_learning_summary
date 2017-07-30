<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Introduction
* auto-gen TOC:
{:toc}

## The Reinforcement Learning Problem
* RL is learning from interaction.
* There is no supervisor, only signals of reward/evaluative feedback.
* Rewards are delayed
* Decisions in sequence does matter as they affect the outcome of
subsequent decisions (non i.i.d).

## Difference to supervised learning
Supervised learning learns from labelled data x ~ y
Reinforcement learning learns from data state-action-reward-following_state
    - predict next state
    - predict reward
    - learn behaviour (which action to choose where)

## Exploration vs Exploitation
* Exploration: explores the environment to gather more data
* Exploitation: exploits the explored information to maximise reward
* Trade-off between exploration vs exploitation is important
