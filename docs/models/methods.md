---
layout: default
title: Reasoning Methods
nav_order: 4
toc_list: true
last_modified_date: April 24 2021
permalink: /methods
---

# Methods to Commonsense Reasoning
{: .no_toc }

Editors: [Bill Yuchen Lin](https://yuchenlin.xyz/), [Yang Qiao](https://www.linkedin.com/in/xiaoyang-qiao/){: target="_blank"}

{: .fs-5 .fw-300 }
We present a collection of insightful research papers that focus on teaching machines to think with common sense like humans. We grouped them in different categories mainly based on the knowledge resources they used. 


 
## Table of contents
{: .no_toc .text-delta .fs-4 style="font-weight:800"}

- TOC
{:toc}


**Tags:**

- `supervised`{: .method-label}, `unsupervised`{: .method-label}: whether the method needs to use the training data (annotated by humans) of the target task.
- `data-augmentation`{: .method-label}: this method introduces a way to automatically generate more supervision for learning commonsense reasoning models.
- `coreference`{: .method-label}, `multiple-choice`{: .method-label}, `generation`{: .method-label}: the format of the target task. 
- `multi-task`{: .method-label}: the method aims to solve multiple commonsense tasks with a single model.
- `text-to-text`{: .method-label}: the method is based on a text-to-text Transformer (e.g., BART, T5), which is thus usually suitable for all task formats.
- `pre-training`{: .method-label}: the method introduces new pre-training tasks.
- `lm+gnn`{: .method-label}: this method has two components --- a language model (e.g., BERT) and a graph-based reasoning module.
- `kg-aware`{: .method-label}: the method has the access to external commonsense knowledge graphs (e.g., ConceptNet).
- `interpretable`{: .method-label}: the method produces explanations for interpreting its predictions.

---

## LM-only Methods

<table>
<td>
<span class="fs-4">
This line of research focuses on how we can use a language model to solve commonsense reasoning tasks without the access to external knowledge resources. 
</span>
</td>
</table>


{: .fs-4 .fw-800 .text-blue-100}
**📜 A Simple Method for Commonsense Reasoning**. <br> ✍ Trieu H. Trinh, Quoc V. Le *(arXiv 2018)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/1806.02847){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/tensorflow/models/blob/a6fb124d54365e58b6b4c49219593da4fd3d615b/research/lm_commonsense/README.md){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/A-Simple-Method-for-Commonsense-Reasoning-Trinh-Le/d7b6753a2d4a2b286c396854063bde3a91b75535){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [WSC](/docs/datasets#wsc){: .mr-1 target="_blank"} 

**Tags:** `unsupervised`{: .method-label}, `coreference`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Commonsense reasoning is a long-standing challenge for deep learning. For example, it is difficult to use neural networks to tackle the Winograd Schema dataset (Levesque et al., 2011). In this paper, we present a simple method for commonsense reasoning with neural networks, using unsupervised learning. Key to our method is the use of language models, trained on a massive amount of unlabled data, to score multiple choice questions posed by commonsense reasoning tests. On both Pronoun Disambiguation and Winograd Schema challenges, our models outperform previous state-of-the-art methods by a large margin, without using expensive annotated knowledge bases or hand-engineered Tags. We train an array of large RNN language models that operate at word or character level on LM-1-Billion, CommonCrawl, SQuAD, Gutenberg Books, and a customized corpus for this task and show that diversity of training data plays an important role in test performance. Further analysis also shows that our system successfully discovers important Tags of the context that decide the correct answer, indicating a good grasp of commonsense knowledge.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
  - There is another version on OpenReview.net named [*Do Language Models Have Common Sense?*](https://openreview.net/forum?id=rkgfWh0qKX){: target="_blank"}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 


{: .fs-4 .fw-800 .text-blue-100}
**📜 Attention Is (not) All You Need for Commonsense Reasoning**. <br> ✍ Tassilo Klein, Moin Nabi *(ACL 2019)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/1905.13497){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/SAP-samples/acl2019-commonsense){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Attention-Is-(not)-All-You-Need-for-Commonsense-Klein-Nabi/8e82dd83df5023df86868c59a03fd7872fb5931e){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [WSC](/docs/datasets#wsc){: .mr-1 target="_blank"} 

**Tags:** `unsupervised`{: .method-label}, `coreference`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  The recently introduced BERT model exhibits strong performance on several language understanding benchmarks. In this paper, we describe a simple re-implementation of BERT for commonsense reasoning. We show that the attentions produced by BERT can be directly utilized for tasks such as the Pronoun Disambiguation Problem and Winograd Schema Challenge. Our proposed attention-guided commonsense reasoning method is conceptually simple yet empirically powerful. Experimental analysis on multiple datasets demonstrates that our proposed system performs remarkably well on all cases while outperforming the previously reported state of the art by a margin. While results suggest that BERT seems to implicitly learn to establish complex relationships between entities, solving commonsense reasoning tasks might require more than unsupervised models learned from huge text corpora.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 


{: .fs-4 .fw-800 .text-blue-100}
**📜 Pre-training Text-to-Text Transformers for Concept-centric Common Sense**. <br> ✍ Wangchunshu Zhou, Dong-Ho Lee, Ravi Kiran Selvam, Seyeon Lee, Bill Yuchen Lin, Xiang Ren *(ICLR 2021)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/2011.07956){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/INK-USC/CALM){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Pre-training-Text-to-Text-Transformers-for-Common-Zhou-Lee/fffe61fbd225b59d084148611c49585860e24728){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [OpenbookQA](/docs/datasets#openbookqa){: .mr-1 target="_blank"}, [PIQA](/docs/datasets#physicaliqa){: .mr-1 target="_blank"}, [aNLI](/docs/datasets#anli){: .mr-1 target="_blank"}, [CommonGEN](/docs/datasets#commongen){: .mr-1 target="_blank"}

**Tags**: `pre-training`{: .method-label}, `supervised`{: .method-label}, `text-to-text`{: .method-label}, `multi-task`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Pre-trained language models (PTLM) have achieved impressive results in a range of natural language understanding (NLU) and generation (NLG) tasks. However, current pre-training objectives such as masked token prediction (for BERT-style PTLMs) and masked span infilling (for T5-style PTLMs) do not explicitly model the relational commonsense knowledge about everyday concepts, which is crucial to many downstream tasks that need common sense to understand or generate. To augment PTLMs with concept-centric commonsense knowledge, in this paper, we propose both generative and contrastive objectives for learning common sense from the text, and use them as intermediate self-supervised learning tasks for incrementally pre-training PTLMs (before task-specific fine-tuning on downstream datasets). Furthermore, we develop a joint pre-training framework to unify generative and contrastive objectives so that they can mutually reinforce each other. Extensive experimental results show that our method, concept-aware language model (CALM), can pack more commonsense knowledge into the parameters of a pre-trained text-to-text transformer without relying on external knowledge graphs, yielding better performance on both NLU and NLG tasks. We show that while only incrementally pre-trained on a relatively small corpus for a few steps, CALM outperforms baseline methods by a consistent margin and even comparable with some larger PTLMs, which suggests that CALM can serve as a general, plug-and-play method for improving the commonsense reasoning ability of a PTLM.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}

<hr class="thin" /> 

{: .fs-4 .fw-800 .text-blue-100}
**📜 UnifiedQA: Crossing Format Boundaries With a Single QA System**. <br> ✍ Daniel Khashabi, Sewon Min, Tushar Khot, Ashish Sabharwal, Oyvind Tafjord, Peter Clark, Hannaneh Hajishirzi *(EMNLP 2020 Findings)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/2005.00700){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/allenai/unifiedqa){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/UnifiedQA%3A-Crossing-Format-Boundaries-With-a-Single-Khashabi-Min/d286f3fe4234b017a6c06a72db2599f56b188c43){: .btn .btn-purple .mr-1 target="_blank" }
   [Demo](https://unifiedqa.apps.allenai.org/){: .btn .btn-yellow .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [ARC](/docs/datasets#arc){: .mr-1 target="_blank"}, [OpenbookQA](/docs/datasets#openbookqa){: .mr-1 target="_blank"}, [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, etc.

**Tags**: `pre-training`{: .method-label}, `supervised`{: .method-label}, `text-to-text`{: .method-label}, `multi-task`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Question answering (QA) tasks have been posed using a variety of formats, such as extractive span selection, multiple choice, etc. This has led to format-specialized models, and even to an implicit division in the QA community. We argue that such boundaries are artificial and perhaps unnecessary, given the reasoning abilities we seek to teach are not governed by the format. As evidence, we use the latest advances in language modeling to build a single pre-trained QA model, UnifiedQA, that performs surprisingly well across 17 QA datasets spanning 4 diverse formats. UnifiedQA performs on par with 9 different models that were trained on individual datasets themselves. Even when faced with 12 unseen datasets of observed formats, UnifiedQA performs surprisingly well, showing strong generalization from its out-of-format training data. Finally, simply fine-tuning this pre-trained QA model into specialized models results in a new state of the art on 6 datasets, establishing UnifiedQA as a strong starting point for building QA systems.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
 

<!-- 
2. Attention Is (not) All You Need for Commonsense Reasoning 
  https://arxiv.org/abs/1905.13497 ACL 2019
  https://github.com/SAP-samples/acl2019-commonsense 
  Tasks: WSC

3. Pre-training Text-to-Text Transformers for Concept-centric Common Sense
ICLR 2021
 -->

--- 

## KG-aware Methods

<table>
<td>
<span class="fs-4">
These methods uses external commonsense knowledge as during the training and inference time. They usually fist retrieve relevant commonsense knowledge from external KGs (e.g., ConceptNet), which are usually in graph structures, and then employ a graph-based neural reasoner.
</span>
</td>
</table>

{: .fs-4 .fw-800 .text-blue-100}
**📜 KagNet: Knowledge-Aware Graph Networks for Commonsense Reasoning**. <br> ✍ Bill Yuchen Lin, Xinyue Chen, Jamin Chen, Xiang Ren *(EMNLP 2019)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/1909.02151){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/INK-USC/KagNet){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/KagNet%3A-Knowledge-Aware-Graph-Networks-for-Lin-Chen/710d183174844da5b7f392667f3cc25d2b098dde){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"} 

**Tags**: `supervised`{: .method-label}, `lm+gnn`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}, `interpretable`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Commonsense reasoning aims to empower machines with the human ability to make presumptions about ordinary situations in our daily life. In this paper, we propose a textual inference framework for answering commonsense questions, which effectively utilizes external, structured commonsense knowledge graphs to perform explainable inferences. The framework first grounds a question-answer pair from the semantic space to the knowledge-based symbolic space as a schema graph, a related sub-graph of external knowledge graphs. It represents schema graphs with a novel knowledge-aware graph network module named KagNet, and finally scores answers with graph representations. Our model is based on graph convolutional networks and LSTMs, with a hierarchical path-based attention mechanism. The intermediate attention scores make it transparent and interpretable, which thus produce trustworthy inferences. Using ConceptNet as the only external resource for Bert-based models, we achieved state-of-the-art performance on the CommonsenseQA, a large-scale dataset for commonsense reasoning.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 


{: .fs-4 .fw-800 .text-blue-100}
**📜 Scalable Multi-Hop Relational Reasoning for Knowledge-Aware Question Answering**. <br> ✍ Yanlin Feng, Xinyue Chen, Bill Yuchen Lin, Peifeng Wang, Jun Yan, Xiang Ren *(EMNLP 2020)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/2005.00646){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/INK-USC/MHGRN){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/Scalable-Multi-Hop-Relational-Reasoning-for-Feng-Chen/9e979667aa81c294062c02ab3a48e87e47c54987){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [OpenbookQA](/docs/datasets#openbookqa){: .mr-1 target="_blank"} 

**Tags**: `supervised`{: .method-label}, `lm+gnn`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}, `interpretable`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Existing work on augmenting question answering (QA) models with external knowledge (e.g., knowledge graphs) either struggle to model multi-hop relations efficiently, or lack transparency into the model's prediction rationale. In this paper, we propose a novel knowledge-aware approach that equips pre-trained language models (PTLMs) with a multi-hop relational reasoning module, named multi-hop graph relation network (MHGRN). It performs multi-hop, multi-relational reasoning over subgraphs extracted from external knowledge graphs. The proposed reasoning module unifies path-based reasoning methods and graph neural networks to achieve better interpretability and scalability. We also empirically show its effectiveness and scalability on CommonsenseQA and OpenbookQA datasets, and interpret its behaviors with case studies.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 

{: .fs-4 .fw-800 .text-blue-100}
**📜 Connecting the Dots: A Knowledgeable Path Generator for Commonsense Question Answering**. <br> ✍ Peifeng Wang, Nanyun Peng, Filip Ilievski, Pedro Szekely, Xiang Ren *(EMNLP 2020 Findings)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/2005.00691){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/wangpf3/Commonsense-Path-Generator){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/Connecting-the-Dots%3A-A-Knowledgeable-Path-Generator-Wang-Peng/ab7ab14f07321f6338c6f2364d3d3a46bf2045e2){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [OpenbookQA](/docs/datasets#openbookqa){: .mr-1 target="_blank"} 

**Tags**: `supervised`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}, `interpretable`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Commonsense question answering (QA) requires background knowledge which is not explicitly stated in a given context. Prior works use commonsense knowledge graphs (KGs) to obtain this knowledge for reasoning. However, relying entirely on these KGs may not suffice, considering their limited coverage and the contextual dependence of their knowledge. In this paper, we augment a general commonsense QA framework with a knowledgeable path generator. By extrapolating over existing paths in a KG with a state-of-the-art language model, our generator learns to connect a pair of entities in text with a dynamic, and potentially novel, multi-hop relational path. Such paths can provide structured evidence for solving commonsense questions without fine-tuning the path generator. Experiments on two datasets show the superiority of our method over previous works which fully rely on knowledge from KGs (with up to 6% improvement in accuracy), across various amounts of training data. Further evaluation suggests that the generated paths are typically interpretable, novel, and relevant to the task.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 


{: .fs-4 .fw-800 .text-blue-100}
**📜 Graph-Based Reasoning over Heterogeneous External Knowledge for Commonsense Question Answering**. <br> ✍ Shangwen Lv, Daya Guo, Jingjing Xu, Duyu Tang, Nan Duan, Ming Gong, Linjun Shou, Daxin Jiang, Guihong Cao, Songlin Hu *(AAAI 2020)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/1909.05311){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/DecstionBack/AAAI_2020_CommonsenseQA){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/Graph-Based-Reasoning-over-Heterogeneous-External-Lv-Guo/2e840854bcd7ff47f77acd9f88b61aba40560105){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"} 

**Tags**: `supervised`{: .method-label}, `lm+gnn`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}, `interpretable`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Commonsense question answering aims to answer questions which require background knowledge that is not explicitly expressed in the question. The key challenge is how to obtain evidence from external knowledge and make predictions based on the evidence. Recent works either learn to generate evidence from human-annotated evidence which is expensive to collect, or extract evidence from either structured or unstructured knowledge bases which fails to take advantages of both sources. In this work, we propose to automatically extract evidence from heterogeneous knowledge sources, and answer questions based on the extracted evidence. Specifically, we extract evidence from both structured knowledge base (i.e. ConceptNet) and Wikipedia plain texts. We construct graphs for both sources to obtain the relational structures of evidence. Based on these graphs, we propose a graph-based approach consisting of a graph-based contextual word representation learning module and a graph-based inference module. The first module utilizes graph structural information to re-define the distance between words for learning better contextual word representations. The second module adopts graph convolutional network to encode neighbor information into the representations of nodes, and aggregates evidence with graph attention mechanism for predicting the final answer. Experimental results on CommonsenseQA dataset illustrate that our graph-based approach over both knowledge sources brings improvement over strong baselines. Our approach achieves the state-of-the-art accuracy (75.3%) on the CommonsenseQA leaderboard.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 

{: .fs-4 .fw-800 .text-blue-100}
**📜 Towards Generalizable Neuro-Symbolic Systems for Commonsense Question Answering**. <br> ✍ Kaixin Ma, Jonathan Francis, Quanyang Lu, Eric Nyberg, Alessandro Oltramari *(EMNLP-COIN 2019)*
 

<span class="fs-2">
   [Paper](https://arxiv.org/abs/1910.14087){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/Mayer123/HyKAS){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/Towards-Generalizable-Neuro-Symbolic-Systems-for-Ma-Francis/a078d53c1eff50123e2b065276663de539a40aa1){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [DREAM](https://arxiv.org/abs/1902.00164){: .mr-1 target="_blank"}

**Tags**: `supervised`{: .method-label}, `lm+gnn`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}, `interpretable`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Non-extractive commonsense QA remains a challenging AI task, as it requires systems to reason about, synthesize, and gather disparate pieces of information, in order to generate responses to queries. Recent approaches on such tasks show increased performance, only when models are either pre-trained with additional information or when domain-specific heuristics are used, without any special consideration regarding the knowledge resource type. In this paper, we perform a survey of recent commonsense QA methods and we provide a systematic analysis of popular knowledge resources and knowledge-integration methods, across benchmarks from multiple commonsense datasets. Our results and analysis show that attention-based injection seems to be a preferable choice for knowledge integration and that the degree of domain overlap, between knowledge bases and datasets, plays a crucial role in determining model success.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 

{: .fs-4 .fw-800 .text-blue-100}
**📜 KG-BART: Knowledge Graph-Augmented BART for Generative Commonsense Reasoning**. <br> ✍ Ye Liu, Yao Wan, Lifang He, Hao Peng, Philip S. Yu *(AAAI 2021)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/2009.12677){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/yeliu918/KG-BART){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/KG-BART%3A-Knowledge-Graph-Augmented-BART-for-Liu-Wan/997887cff41577752dc832e9475d5bb22c265093){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonGEN](/docs/datasets#commongen){: .mr-1 target="_blank"} 


**Tags**: `supervised`{: .method-label}, `lm+gnn`{: .method-label}, `kg-aware`{: .method-label}, `text-generation`{: .method-label}, `interpretable`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Generative commonsense reasoning which aims to empower machines to generate sentences with the capacity of reasoning over a set of concepts is a critical bottleneck for text generation. Even the state-of-the-art pre-trained language generation models struggle at this task and often produce implausible and anomalous sentences. One reason is that they rarely consider incorporating the knowledge graph which can provide rich relational information among the commonsense concepts. To promote the ability of commonsense reasoning for text generation, we propose a novel knowledge graph augmented pre-trained language generation model KG-BART, which encompasses the complex relations of concepts through the knowledge graph and produces more logical and natural sentences as output. Moreover, KG-BART can leverage the graph attention to aggregate the rich concept semantics that enhances the model generalization on unseen concept sets. Experiments on benchmark CommonGen dataset verify the effectiveness of our proposed approach by comparing with several strong pre-trained language generation models, particularly KG-BART outperforms BART by 5.80, 4.60, in terms of BLEU-3, 4. Moreover, we also show that the generated context by our model can work as background scenarios to benefit downstream commonsense QA tasks.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
 
 
--- 

## Weak Supervision

<table>
<td>
<span class="fs-4">
The following papers aim to use existing resources to create more supervision (typically in the form of synthetic datasets) for learning commonsense reasoning models with little human annotation effort. The created datasets can be used by the above mentioned methods.
</span>
</td>
</table>

{: .fs-4 .fw-800 .text-blue-100}
**📜 Align, Mask and Select: A Simple Method for Incorporating Commonsense Knowledge into Language Representation Models**. <br> ✍ Zhi-Xiu Ye, Qian Chen, Wen Wang, Zhen-Hua Ling *(arXiv 2019)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/1908.06725){: .btn .btn-blue .mr-1 target="_blank" } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Align%2C-Mask-and-Select%3A-A-Simple-Method-for-into-Ye-Chen/0ff7f557203d1489110b9d2f89a76245def7b530){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [WSC](/docs/datasets#wsc){: .mr-1 target="_blank"}, [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}

**Tags:** `data-augmentation`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  The state-of-the-art pre-trained language representation models, such as Bidirectional Encoder Representations from Transformers (BERT), rarely incorporate commonsense knowledge or other knowledge explicitly. We propose a pre-training approach for incorporating commonsense knowledge into language representation models. We construct a commonsense-related multi-choice question answering dataset for pre-training a neural language representation model. The dataset is created automatically by our proposed "align, mask, and select" (AMS) method. We also investigate different pre-training tasks. Experimental results demonstrate that pre-training models using the proposed approach followed by fine-tuning achieve significant improvements over previous state-of-the-art models on two commonsense-related benchmarks, including CommonsenseQA and Winograd Schema Challenge. We also observe that fine-tuned models after the proposed pre-training approach maintain comparable performance on other NLP tasks, such as sentence classification and natural language inference tasks, compared to the original BERT models. These results verify that the proposed approach, while significantly improving commonsense-related NLP tasks, does not degrade the general language representation capabilities.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}
<hr class="thin" /> 

{: .fs-4 .fw-800 .text-blue-100}
**📜 Generative Data Augmentation for Commonsense Reasoning**. <br> ✍ Yiben Yang, Chaitanya Malaviya, Jared Fernandez, Swabha Swayamdipta, Ronan Le Bras, Ji-Ping Wang, Chandra Bhagavatula, Yejin Choi, Doug Downey *(EMNLP 2020 Findings)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/2004.11546){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/yangyiben/G-DAUG-c-Generative-Data-Augmentation-for-Commonsense-Reasoning){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/Generative-Data-Augmentation-for-Commonsense-Yang-Malaviya/dd6f3b6d92ae9448a2000d9690b921f545f00256){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [WinoGrande](/docs/datasets#winogrande){: .mr-1 target="_blank"}, [CODAH](/docs/datasets#codah){: .mr-1 target="_blank"}, [HellaSwag](/docs/datasets#swag-and-hellaswag){: .mr-1 target="_blank"}

**Tags:** `data-augmentation`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Recent advances in commonsense reasoning depend on large-scale human-annotated training data to achieve peak performance. However, manual curation of training examples is expensive and has been shown to introduce annotation artifacts that neural models can readily exploit and overfit on. We investigate G-DAUG^C, a novel generative data augmentation method that aims to achieve more accurate and robust learning in the low-resource setting. Our approach generates synthetic examples using pretrained language models, and selects the most informative and diverse set of examples for data augmentation. In experiments with multiple commonsense reasoning benchmarks, G-DAUG^C consistently outperforms existing data augmentation methods based on back-translation, and establishes a new state-of-the-art on WinoGrande, CODAH, and CommonsenseQA. Further, in addition to improvements in in-distribution accuracy, G-DAUG^C-augmented training also enhances out-of-distribution generalization, showing greater robustness against adversarial or perturbed examples. Our analysis demonstrates that G-DAUG^C produces a diverse set of fluent training examples, and that its selection and training approaches are important for performance. Our findings encourage future research toward generative data augmentation to enhance both in-distribution learning and out-of-distribution generalization.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}


<br> 

{: .fs-4 .fw-800 .text-blue-100}
**📜 Knowledge-driven Data Construction for Zero-shot Evaluation in Commonsense Question Answering**. <br> ✍ Kaixin Ma, Filip Ilievski, Jonathan Francis, Yonatan Bisk, Eric Nyberg, Alessandro Oltramari
 *(AAAI 2021)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/abs/2011.03863){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/Mayer123/HyKAS-CSKG){: target="_blank" .btn .btn-green .mr-1 }
   [Semantic Scholar](https://www.semanticscholar.org/paper/Knowledge-driven-Data-Construction-for-Zero-shot-in-Ma-Ilievski/c3b7714572bee365eef4f4dfa1839fa5a6ec2dea){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Evaluation Tasks:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [aNLI](/docs/datasets#anli){: .mr-1 target="_blank"}, [PhysicalIQA](/docs/datasets#physicaliqa){: .mr-1 target="_blank"}, [SocialIQA](/docs/datasets#socialiqa){: .mr-1 target="_blank"}, [WinoGrande](/docs/datasets#winogrande){: .mr-1 target="_blank"}

**Tags:** `data-augmentation`{: .method-label}, `kg-aware`{: .method-label}, `multiple-choice`{: .method-label}

<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Recent developments in pre-trained neural language modeling have led to leaps in accuracy on commonsense question-answering benchmarks. However, there is increasing concern that models overfit to specific tasks, without learning to utilize external knowledge or perform general semantic reasoning. In contrast, zero-shot evaluations have shown promise as a more robust measure of a model's general reasoning abilities. In this paper, we propose a novel neuro-symbolic framework for zero-shot question answering across commonsense tasks. Guided by a set of hypotheses, the framework studies how to transform various pre-existing knowledge resources into a form that is most effective for pre-training models. We vary the set of language models, training regimes, knowledge sources, and data generation strategies, and measure their impact across tasks. Extending on prior work, we devise and compare four constrained distractor-sampling strategies. We provide empirical results across five commonsense question-answering tasks with data generated from five external knowledge resources. We show that, while an individual knowledge graph is better suited for specific tasks, a global knowledge graph brings consistent gains across different tasks. In addition, both preserving the structure of the task as well as generating fair and informative questions help language models learn more effectively.
  ``` 
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}

<!-- 
1. Align, Mask and Select: A Simple Method for Incorporating Commonsense Knowledge into Language Representation Models
 https://arxiv.org/abs/1908.06725

2. Generative Data Augmentation for Commonsense Reasoning ( EMNLP 2020 Findings)
Code: https://github.com/yangyiben/G-DAUG-c-Generative-Data-Augmentation-for-Commonsense-Reasoning

3. Knowledge-driven Data Construction for Zero-shot Evaluation in Commonsense Question Answering (AAAI 2021)
https://github.com/Mayer123/HyKAS-CSKG
 -->
---

<!-- ## Rule-based Reasoning -->

<!-- Pending -->


## Others


