# Temporal Difference

<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Outline
* auto-gen TOC:
{:toc}

## Intro model-free
* It learns only values like 
{% raw %}
$$ V(s), Q(s,a) $$
{% endraw %}
* instead of 
{% raw %}
$$ P(s'|a,s), R(s,a) $$
{% endraw %}
* (which would be model-based)

## Monte-Carlo Learning
* For learning how good one policy is
* Will only update believe after whole episode

![Monte Carlo Policy Evaluation](http://incompleteideas.net/sutton/book/ebook/pseudotmp3.png)

## Temporal-Difference (TD) Learning
* vs MC: also update during episode 

> TD methods learn their estimates in part on the basis of other estimates. They learn a guess from a guess--they bootstrap.

![TD learning](http://incompleteideas.net/sutton/book/ebook/pseudotmp7.png)

## SARSA
* __State-Action-Reward-State'-Action'__
* on-policy

> This update is done after every transition from a nonterminal state . If  is terminal, then  is defined as zero. This rule uses every element of the quintuple of events, , that make up a transition from one state-action pair to the next. This quintuple gives rise to the name Sarsa for the algorithm.
> 
{% raw %}
$$ Q(s_t,a_t) = Q(s_t,a_t) + \alpha [r_{t+q} + \lambda Q(s_{t+1},a_{t+1}) - Q(s_t,a_t)] $$
{% endraw %}

![Sarsa](http://incompleteideas.net/sutton/book/ebook/pseudotmp8.png)

### Excourse: ε-Greedy Policy
with probability 1-ε:
{% raw %}
$$ a = argmax_{a' \in A}Q(s,a') $$
{% endraw %}
with probability ε:
{% raw %}
$$ a = rand(A) $$
{% endraw %}

## Q-learning
* off-policy 
* it is no necessary to learn with the policy you will use

![Q Learning](http://incompleteideas.net/sutton/book/ebook/pseudotmp9.png)

### Q-larning vs SARSA
(On the cliff walking example)
> After an initial transient, Q-learning learns values for the optimal policy, that which travels right along the edge of the cliff. Unfortunately, this results in its occasionally falling off the cliff because of the $\varepsilon $-greedy action selection. Sarsa, on the other hand, takes the action selection into account and learns the longer but safer path through the upper part of the grid. Although Q-learning actually learns the values of the optimal policy, its on-line performance is worse than that of Sarsa, which learns the roundabout policy. Of course, if $\varepsilon $ were gradually reduced, then both methods would asymptotically converge to the optimal policy.

## Eligibility Traces
### Sarsa(λ)
> One-step Sarsa and Sarsa(λ) are on-policy algorithms, meaning that they approximate {% raw %}$q_\pi(s, a)${% endraw %}, the action values for the current policy, π, then improve the policy gradually based on the approximate values for the current policy. The policy improvement can be done in many different ways, as we have seen.

![SARSA lambda](http://incompleteideas.net/sutton/book/ebook/pseudotmp12.png "SARSA lambda")

### Q(λ)
> Q($\lambda $) does not look ahead all the way to the end of the episode in its backup. It only looks ahead as far as the next exploratory action.

![Q lambda](http://incompleteideas.net/sutton/book/ebook/pseudotmp13.png)
