<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Outline
* auto-gen TOC:
{:toc}

## Intro 
* Tabular methods use discrete space
* This might be infeasible for big environments
* It is basically ML

## Supervised Learning Formulation
To use RL with this we need to find a parameter vector that represents the data. This can be achieved with supervised learning. We need to minimize the error of the parametrized value function V(s;θ):
{% raw %}
$$ L(\theta) = E[(V^\pi(s) - V(s,\theta))^2] $$
{% endraw %}
This can be done analytically with the partial derivative ![](http://incompleteideas.net/sutton/book/ebook/inimgtmp1318.png) :
{% raw %}
$$ \theta_{t+1} = \theta_t + \alpha_t(V^\pi(s) - V(s,\theta)) \bigtriangledown_{\theta_t} V_t(s_t) $$
{% endraw %}

## TD(λ)

![TD lambda gradient-descent](http://incompleteideas.net/sutton/book/ebook/pseudotmp14.png)

Here V is implicitly a function of θ
