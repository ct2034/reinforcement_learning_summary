<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Inverse Reinforcement Learning
* auto-gen TOC:
{:toc}

## Intro
* Develop a policy based on observations of optimal behaviour
* Learning from Demonstration

## Max Margin Formulation
The margin between π^* and π needs to decrease (logically)
![](https://farm5.staticflickr.com/4318/36230885916_48c1ac9339_z_d.jpg)

[[source: Abbeel]](https://ct2034.github.io/reinforcement_learning_summary/references.html#abbeel-inverse-rl-slides)

* problem when big number of constraints

## Reward Formulation
Get an R that satisfies:
![](https://farm5.staticflickr.com/4291/35439638384_1c9681b394_z_d.jpg)

[[source: Abbeel]](https://ct2034.github.io/reinforcement_learning_summary/references.html#abbeel-inverse-rl-slides)

* better for large domains
