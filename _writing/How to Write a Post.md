---
title: "How to Write a Post"
description: A sample showing headings, math, code, images, and tables. It stays private because published is false.
date: 2026-11-24
tags: [meta]
published: false
---

This post is never shown on the site because `published` is unchecked. Use it as a reference.

## Writing a new post in Obsidian

1. Press **Ctrl+N**. A new note opens in `_writing`.
2. Type the title as the note's name.
3. Press **Alt+T** to fill in the post template.
4. Write. Turn on **published** when it's ready.
5. Click **Commit-and-sync** in the left sidebar (the Obsidian Git icon). It's live in about a minute.

### Headings make the table of contents

Every `##` and `###` heading appears in the collapsible Table of Contents.

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

Paste an image (Ctrl+V) or drag it in. Obsidian saves it to `assets/img/` and the link works on the site as-is.
