---
layout: default
title: Reasoning Methods
nav_order: 4
toc_list: true
last_modified_date: March 26 2021
permalink: /docs/methods
---

# Reasoning Methods
{: .no_toc }

Editors: [Bill Yuchen Lin](https://yuchenlin.xyz/), 

{: .fs-5 .fw-300 }
We present a collection of insightful research papers that focus on teaching machines to think with common sense like humans. We grouped them in different categories mainly based on the knowledge resources they used. 


---

## LM-only Methods


Here we present methods that only use language models to address the chellenge of commonsense reasoning. 
 
 
<br> 


{: .fs-4 .fw-800 .text-blue-100}
**📜 A Simple Method for Commonsense Reasoning**. <br> ✍ Trieu H. Trinh, Quoc V. Le *(arXiv 2018)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/1806.02847){: .btn .btn-blue .mr-1 target="_blank" } [Code](https://github.com/tensorflow/models/blob/a6fb124d54365e58b6b4c49219593da4fd3d615b/research/lm_commonsense/README.md){: target="_blank" .btn .btn-green .mr-1 }
</span> 

Evaluation Tasks: [WSC](/docs/datasets/#wsc){: .mr-1 target="_blank"} 
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Commonsense reasoning is a long-standing challenge for deep learning. For example, it is difficult to use neural networks to tackle the Winograd Schema dataset (Levesque et al., 2011). In this paper, we present a simple method for commonsense reasoning with neural networks, using unsupervised learning. Key to our method is the use of language models, trained on a massive amount of unlabled data, to score multiple choice questions posed by commonsense reasoning tests. On both Pronoun Disambiguation and Winograd Schema challenges, our models outperform previous state-of-the-art methods by a large margin, without using expensive annotated knowledge bases or hand-engineered features. We train an array of large RNN language models that operate at word or character level on LM-1-Billion, CommonCrawl, SQuAD, Gutenberg Books, and a customized corpus for this task and show that diversity of training data plays an important role in test performance. Further analysis also shows that our system successfully discovers important features of the context that decide the correct answer, indicating a good grasp of commonsense knowledge.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Editors' comments</summary>
  {: .fs-3 .text-delta .text-red-100}
  - There is another version on OpenReview.net named [*Do Language Models Have Common Sense?*](https://openreview.net/forum?id=rkgfWh0qKX){: target="_blank"}
</details> 
{: .fs-3 .fw-600 .text-red-300}
 
<br> 


<!-- 
1. Attention Is (not) All You Need for Commonsense Reasoning 
  https://arxiv.org/abs/1905.13497 ACL 2019
  https://github.com/SAP-samples/acl2019-commonsense 
  Tasks: WSC

2. 

 -->

--- 

## KG-aware Methods

--- 

## Weak Supervision

---

## Rule-based Reasoning



