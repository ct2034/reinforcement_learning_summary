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
* For learning how good one policy on a certain state is

![Monte Carlo Policy Evaluation](http://incompleteideas.net/sutton/book/ebook/pseudotmp3.png)

## Temporal-Difference (TD) Learning

## SARSA
![SARSA lambda](http://incompleteideas.net/sutton/book/ebook/pseudotmp12.png "SARSA lambda")

## Q-learning

## Eligibility Traces

