<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Introduction
* auto-gen TOC:
{:toc}

## The Agent-Environment Interface

## Markov Decision Process
* Formulation
* Optimality
* Markov **Reward** Process (MRP) = MDP + a fixed policy

![](https://farm5.staticflickr.com/4327/35440549924_4555de2502_z_d.jpg)

## Value Function
![](https://farm5.staticflickr.com/4319/36231776966_623184503e_z_d.jpg)

![](https://farm5.staticflickr.com/4291/36231777896_6df7b07fee_z_d.jpg)

[[source: udacity]](https://ct2034.github.io/reinforcement_learning_summary/references.html#udacity-course-reinforcement-learning)

## Action-Value Function
![](https://farm5.staticflickr.com/4318/35440550364_9d7ee793cc_z_d.jpg)
![](https://farm5.staticflickr.com/4296/36140063171_af43038cee_z_d.jpg)

[[source: udacity]](https://ct2034.github.io/reinforcement_learning_summary/references.html#udacity-course-reinforcement-learning)

## VI vs. PI
* VI is PI with one step of policy evaluation.
* PI converges surprisingly rapildy, however with expensive compution, i.e. the policy evaluation step (wait for convergence of V^π).
* PI is prefered if the action set is large.

## Asynchronous Dynamic Programming
* The value function table is updated asynchronously.
* Computation is significantly reduced.
* If all states are updated infinitely, convergence is still guaranteed.
* Three simple algorithms:
    - Gauss-Seidel Value Iteration
    - Real-time dynamic programming
    - Prioritised sweeping

![](https://farm5.staticflickr.com/4325/36231779686_386a575e8c_z_d.jpg)
![](https://farm5.staticflickr.com/4313/35440552004_d79499c6f8_z_d.jpg)
![](https://farm5.staticflickr.com/4323/36231780096_2b5d2ed62c_z_d.jpg)
![](https://farm5.staticflickr.com/4293/35440552354_f008c272c5_z_d.jpg)
