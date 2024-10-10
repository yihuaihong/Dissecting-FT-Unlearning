# Dissecting-FT-Unlearning (EMNLP 2024 Main - Short)

The code for the experiments in our paper titled **[Dissecting Fine-Tuning Unlearning in Large Language Models]** accepted in EMNLP 2024 Main (Short paper)

* **Arxiv:** https://arxiv.org/abs/2410.06606




## Quick Links
- [Dissecting FT Unlearning](#Dissecting-FT-Unlearning)
  - [Quick Links](#quick-links)
  - [Overview](#overview)
  - [1. Requirements](#1-requirements)
  - [2. Training and Forgetting](#2-training-and-forgetting)
  - [3. Evaluate Forgetting Effectiveness](#3-evaluate-forgetting-effectiveness)
  - [How to Cite](#how-to-cite)

## Overview
You can reproduce the experiments in our paper.

> **Abstract**
> Fine-tuning-based unlearning methods prevail for preventing targeted harmful, sensitive, or copyrighted information within large language models while preserving overall capabilities. However, the true effectiveness of these methods is unclear.  In this paper, we delve into the limitations of fine-tuning-based unlearning through activation patching and parameter restoration experiments. Our findings reveal that these methods alter the model's knowledge retrieval process, rather than genuinely erasing the problematic knowledge embedded in the model parameters. Furthermore, behavioral tests demonstrate that the unlearning mechanisms inevitably impact the global behavior of the models, affecting unrelated knowledge or capabilities.  Our work advocates the development of more resilient unlearning techniques for truly erasing knowledge.
