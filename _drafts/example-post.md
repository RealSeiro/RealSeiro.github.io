---
title: "Example Post: How Writing Works Here"
description: A template showing headings, math, code, images, and tables. Copy it into _posts/ with a date to publish.
tags: [meta]
---

Files in `_drafts/` are never published. To publish a post, copy this file into `_posts/` and name it `YYYY-MM-DD-your-title.md`.

## Headings make the table of contents

Every `##` and `###` heading shows up in the collapsible **Table of Contents** at the top of the post.

### A smaller heading

Like this one.

## Math

Inline math goes between double dollar signs: the policy gradient is $$\nabla_\theta J(\theta) = \mathbb{E}\left[\nabla_\theta \log \pi_\theta(a \mid s)\, A(s,a)\right]$$.

A display equation sits on its own lines:

$$
\mathcal{L}^{\text{CLIP}}(\theta) = \mathbb{E}_t\Big[\min\big(r_t(\theta)\hat A_t,\ \operatorname{clip}(r_t(\theta), 1-\epsilon, 1+\epsilon)\hat A_t\big)\Big]
$$

## Code

```python
import torch

def td_advantage(rewards, values, gamma=0.99):
    """One-step TD advantage."""
    next_v = torch.cat([values[1:], values.new_zeros(1)])
    return rewards + gamma * next_v - values
```

## Tables and quotes

| Method | Success rate |
|---|---|
| Baseline | 0.42 |
| + Beliefs | 0.57 |

> A quote looks like this.

## Images

Put the file in `assets/img/` and write:

```markdown
![What the figure shows](/assets/img/figure.png)
```
