---
title: "Hello, world"
subtitle: The first post — and a check that math, code, and 한국어 all render.
tags: [meta]
---

This blog is where I'll keep notes on what I'm reading and building in AI research.

## Math

Inline math goes between double dollar signs: the policy-gradient estimate is $$\nabla_\theta J(\theta) = \mathbb{E}\left[\nabla_\theta \log \pi_\theta(a \mid s)\, A(s,a)\right]$$.

A display equation sits on its own lines:

$$
\mathcal{L}^{\text{CLIP}}(\theta) = \mathbb{E}_t\Big[\min\big(r_t(\theta)\hat A_t,\ \operatorname{clip}(r_t(\theta), 1-\epsilon, 1+\epsilon)\hat A_t\big)\Big]
$$

## Code

```python
import torch

def advantage(rewards, values, gamma=0.99):
    """One-step TD advantage."""
    next_v = torch.cat([values[1:], values.new_zeros(1)])
    return rewards + gamma * next_v - values
```

## 한국어

한글 문장도 이렇게 자연스럽게 섞어 쓸 수 있다. 줄바꿈은 단어 단위로 끊긴다.

> A quote looks like this.
