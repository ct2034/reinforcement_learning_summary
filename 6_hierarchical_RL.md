<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Hierarchical Reinforcement Learning
* auto-gen TOC:
{:toc}

## Intro 
> The structure of the hierarchy is summarized in a task graph, an example of which is given in Figure 2 for a Taxi problem that Dietterich uses as an illustration. Each episode of the overall task consists of picking up, transporting, and dropping off a passenger. The overall problem, corresponding to the root node of the graph, is decomposed into the subtask Get, which is the subtask of going to the passenger’s location and picking them up, and the subtask Put, which is the subtask of going to the passenger’s destination and dropping them off. These subtasks, in turn, are respectively decomposed into the primitive actions Pickup or Dropoff, which respectively pick up and drop off a passenger, and the subtask Navigate(t), which consists of navigating to one of the locations indicated by the parameter t. (A subtask parameterized like this is shorthand for multiple copies of the subtask, one for each value of the parameter.) This subtask Navigate(t) is decomposed into the primitive actions that are moves North, South, East, or West. The subtasks and primitive actions into which a subtask Mi is decomposed are called the “children” of Mi . An important aspect of a task graph is that the order in which a subtask’s children are shown is arbitrary. Which choice the higher level controller makes depends on its policy. The graph just restricts the action choices that can be made at each level

![](https://farm5.staticflickr.com/4321/35438870054_c97fa5d635_z_d.jpg)

[[source: barto]](https://ct2034.github.io/reinforcement_learning_summary/references.html#barto-recent-advances-in-hierarchical-reinforcement-learning)

## SMDP
> In an MDP, only the sequential nature of the decision process is relevant, not the amount of time that passes between decision stages. A generalization of this is the semi-Markov decision process (SMDP) in which the amount of time between one decision and the next is a random variable, either real- or integervalued.
> 
> Let the random variable τ denote the (positive) waiting time for state s when action a is executed. The transition probabilities generalize to give the joint probability that a transition from state s to state s' occurs after τ time steps when action a is executed. We write this joint probability as P(s' , τ |s, a).

Bellman Equations for SMDPS:
![](https://farm5.staticflickr.com/4301/36104970792_cf409ba18e_z_d.jpg)

[[source: barto]](https://ct2034.github.io/reinforcement_learning_summary/references.html#barto-recent-advances-in-hierarchical-reinforcement-learning)

## Options
![](https://farm5.staticflickr.com/4297/36105109322_2af21805d2_z_d.jpg)

> policy π : S× U_S∈S As → [0, 1], a termination condition β : S → [0, 1], and an input set I ⊆ S. The option hI, π, βi is available in state s if and only if s ∈ I. If the option is executed, then actions are selected according to π until the option terminates stochastically according to β.

## MAX-Q
> A subtask is very much like a hierarchical option, hIi , µi , βi i, as defined in Section 4.1, with the addition of a pseudo-reward function. The policy over options, µi , corresponds to the subtask’s πi ; the termination condition, βi , in this case assigns to states termination probabilities of only 1 or 0; and the option’s input set Ii corresponds to Si .

* value decomposition:
* V^π (0, s) = V^π (an, s) + C^π (an−1, s, an) + · · · + C^π (a1, s, a2) + C^π (0, s, a1),
* with completion terms:
C^π (i, s, a) = SUM_{s',τ}  P^π_i (s', τ |s, a)γ τ Q^π (i, s', π(s')).
