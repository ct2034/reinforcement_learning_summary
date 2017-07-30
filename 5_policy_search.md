<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Outline
* auto-gen TOC:
{:toc}

## Intro
* Policy Search uses
    - exploration
    - evaluation
    - updates
* based on experience data
* not model-based
* not learning a value func first

* value based solution inefficient for large or high-dimensional spaces

<iframe width="560" height="315" src="https://www.youtube.com/embed/bJMib3EPwAE" frameborder="0" allowfullscreen></iframe>

![Important slide from video](https://farm5.staticflickr.com/4313/36102858632_afe96bc2ed_z_d.jpg)

[[source: udacity]](https://ct2034.github.io/reinforcement_learning_summary/references.html#udacity-course-reinforcement-learning)

## Difference between Policy Search and Value-based RL
* PS is guaranteed to converge
* good for high dimensional spaces
* can learn from demonstration
Disadvantage of PS: Computationally Inefficient (see video)

## Plain Policy Gradient
```
while (not converged)
  # Exploration:
  Generate Trajectories D using π(θ_k)
  # Evaluation: 
  Check Quality of π(θ_k; D)
  # Update:
  Make π(θ_{k+1}) using evaluations and trajectories
```
or

![](http://incompleteideas.net/sutton/book/ebook/pseudotmp1.png)
[[source: sutton]](https://ct2034.github.io/reinforcement_learning_summary/references.html#sutton-and-barto-reinforcement-learning-an-introduction)


## Likelihood Ratio Gradient

## REINFORCE

## G(PO)MDP

## Gauss-Newton 
* second-order policy gradient

## Natural Gradient-Actor-Critic
## Natural Actor-Critic
