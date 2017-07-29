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

{% raw %}
$$ Q(s_t,a_t) = Q(s_t,a_t) + /alpha [r_{t+q} + /lambda Q(s_{t+1},a_{t+1}) - Q(s_t,a_t)] $$
{% endraw %}

![Sarsa](http://incompleteideas.net/sutton/book/ebook/pseudotmp8.png)

## Q-learning
* off-policy 
* it is no necessary to learn with the policy you will use

## Eligibility Traces
### Sarsa(λ)
> One-step Sarsa and Sarsa(λ) are on-policy algorithms, meaning that they approximate {% raw %}$q_\pi(s, a)${% endraw %}, the action values for the current policy, π, then improve the policy gradually based on the approximate values for the current policy. The policy improvement can be done in many different ways, as we have seen.

![SARSA lambda](http://incompleteideas.net/sutton/book/ebook/pseudotmp12.png "SARSA lambda")

### Q(λ)
> Q($\lambda $) does not look ahead all the way to the end of the episode in its backup. It only looks ahead as far as the next exploratory action.

![Q lambda](http://incompleteideas.net/sutton/book/ebook/pseudotmp13.png)
