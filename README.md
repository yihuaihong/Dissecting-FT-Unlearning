# Dissecting-FT-Unlearning (EMNLP 2024 Main - Short)

The code for the experiments in our paper titled **[Dissecting Fine-Tuning Unlearning in Large Language Models]** accepted in EMNLP 2024 Main (Short paper), which is a follow-up work of [ConceptVectors Benchmark](https://arxiv.org/pdf/2406.11614).

* **Arxiv:** https://arxiv.org/abs/2410.06606




## Quick Links
- [Dissecting FT Unlearning](#Dissecting-FT-Unlearning)
  - [Quick Links](#quick-links)
  - [Overview](#overview)
  - [1. Requirements](#1-requirements)
  - [2. Download Unlearned models](#2-Download-Unlearned-models)
  - [3. Patching or Restoring Experiments](#3-Patching-or-Restoring-Experiments)
  - [How to Cite](#how-to-cite)

## Overview
You can reproduce the experiments in our paper.

> **Abstract**
> Fine-tuning-based unlearning methods prevail for preventing targeted harmful, sensitive, or copyrighted information within large language models while preserving overall capabilities. However, the true effectiveness of these methods is unclear.  In this paper, we delve into the limitations of fine-tuning-based unlearning through activation patching and parameter restoration experiments. Our findings reveal that these methods alter the model's knowledge retrieval process, rather than genuinely erasing the problematic knowledge embedded in the model parameters. Interestingly, the MLP components in the model's final layer are the primary contributors to these apparently positive unlearning effects, responsible for controlling the models' behaviors. Our work advocates the development of more resilient unlearning techniques for truly erasing knowledge. The code is released at https://github.com/yihuaihong/Dissecting-FT-Unlearning


## 1. Requirements
To install the required packages, please run the following command.
```sh
conda install pytorch==2.2.0 torchvision==0.17.0 torchaudio==2.2.0 pytorch-cuda=11.8 -c pytorch -c nvidia
pip install -r requirements.txt
```

## 2. Download Unlearned models 

For convenience, we directly released the models after Unlearning training (via DPO or Gradient Difference) on both LLaMA2-7B-chat and OLMo-7B in the Huggingface links below:

```sh
for method in 'dpo' 'grad_diff':
    for id in 16 18 21 26 27 38 42 47 49 54
        download_link = f{https://huggingface.co/YihuaiHong/llama2-7b_{method}_unlearn_on_id_{id}_concept}
```

or

```sh
for method in 'dpo' 'grad_diff':
    for id in 4 37 40 44 59 77 90 105 141 147
        download_link = f{https://huggingface.co/YihuaiHong/olmo-7b_{method}_unlearn_on_id_{id}_concept}
```


## 3. Patching or Restoring Experiments

Please run Restoration_experiments_llama-30tokens.ipynb or Restoration_experiments_olmo-30tokens.ipynb



## How to Cite
```
@misc{hong2024dissectingfinetuningunlearninglarge,
      title={Dissecting Fine-Tuning Unlearning in Large Language Models}, 
      author={Yihuai Hong and Yuelin Zou and Lijie Hu and Ziqian Zeng and Di Wang and Haiqin Yang},
      year={2024},
      eprint={2410.06606},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2410.06606}, 
}
```
