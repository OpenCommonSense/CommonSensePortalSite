---
layout: default
title: Analysis
nav_order: 5
toc_list: true
last_modified_date: April 24 2021
permalink: /analysis/
---

# Analysis about Commonsense Reasoning
{: .no_toc }

Editors: [Bill Yuchen Lin](https://yuchenlin.xyz/){: target="_blank"}, [Pei Zhou](https://sites.google.com/g.ucla.edu/peizhou/home){: target="_blank"}

{: .fs-5 .fw-300 }
Here we present a collection of papers focusing on the analysis about commonsense knowledge and commonsense reasoning. 


---

## Table of contents
{: .no_toc .text-delta .fs-4 style="font-weight:800"}

- TOC
{:toc}


---

## Analyzing Language Models

|<span class="fs-4">This line of research focuses on understanding whether the pre-trained language models (e.g., BERT) have captured commonsense knowledge, and to what extent they can be used for different types of commonsense reasoning. They usually use the pre-trained LMs as they are (i.e., no fine-tuning) and analyze them by designing probing methods for recalling knowledge or completing a reasoning task.</span>|

 
{: .fs-4 .fw-800 .text-blue-100}
**📜 Language Models as Knowledge Bases?**. <br> ✍ Fabio Petroni, Tim Rocktaschel, Patrick Lewis, Anton Bakhtin, Yuxiang Wu, Alexander H. Miller, Sebastian Riedel *(EMNLP 2019)*
 
<span class="fs-2">
   [Paper](https://www.aclweb.org/anthology/D19-1250.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/facebookresearch/LAMA){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Language-Models-as-Knowledge-Bases-Petroni-Rockt%C3%A4schel/d0086b86103a620a86bc918746df0aa642e2a8a3){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [ConceptNet](https://conceptnet.io/){: .mr-1 target="_blank"}, [DOQ](https://github.com/google-research-datasets/distribution-over-quantities){: .mr-1 target="_blank"}, [WordNet](https://wordnet.princeton.edu/){: .mr-1 target="_blank"}, [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page){: .mr-1 target="_blank"}[Wikidata](https://www.english-corpora.org/googlebooks/){: .mr-1 target="_blank"}


 
<details markdown="block">
  <summary><span></span>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Recent progress in pretraining language models on large textual corpora led to a surge of improvements for downstream NLP tasks. Whilst learning linguistic knowledge, these models may also be storing relational knowledge present in the training data, and may be able to answer queries structured as "fill-in-the-blank" cloze statements. Language models have many advantages over structured knowledge bases: they require no schema engineering, allow practitioners to query about an open class of relations, are easy to extend to more data, and require no human supervision to train. We present an in-depth analysis of the relational knowledge already present (without fine-tuning) in a wide range of state-of-the-art pretrained language models. We find that (i) without fine-tuning, BERT contains relational knowledge competitive with traditional NLP methods that have some access to oracle knowledge, (ii) BERT also does remarkably well on open-domain question answering against a supervised baseline, and (iii) certain types of factual knowledge are learned much more readily than others by standard language model pretraining approaches. The surprisingly strong ability of these models to recall factual knowledge without any fine-tuning demonstrates their potential as unsupervised open-domain QA systems. The code to reproduce our analysis is available at https://github.com/facebookresearch/LAMA
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}

<hr class="thin" />
{: .fs-4 .fw-800 .text-blue-100}
**📜 oLMpics-On What Language Model Pre-training Captures**. <br> ✍ Alon Talmor, Yanai Elazar, Y. Goldberg, Jonathan Berant *(TACL 2020)*
 
<span class="fs-2">
   [Paper](https://www.aclweb.org/anthology/2020.tacl-1.48.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/alontalmor/oLMpics){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/oLMpics-On-What-Language-Model-Pre-training-Talmor-Elazar/75c85b07d31144af5426829ff79b2b061de32124){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [ConceptNet](https://conceptnet.io/){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Recent success of pre-trained language models (LMs) has spurred widespread interest in the language capabilities that they possess. However, efforts to understand whether LM representations are useful for symbolic reasoning tasks have been limited and scattered. In this work, we propose eight reasoning tasks, which conceptually require operations such as comparison, conjunction, and composition. A fundamental challenge is to understand whether the performance of a LM on a task should be attributed to the pre-trained representations or to the process of fine-tuning on the task data. To address this, we propose an evaluation protocol that includes both zero-shot evaluation (no fine-tuning), as well as comparing the learning curve of a fine-tuned LM to the learning curve of multiple controls, which paints a rich picture of the LM capabilities. Our main findings are that: (a) different LMs exhibit qualitatively different reasoning abilities, e.g., RoBERTa succeeds in reasoning tasks where BERT fails completely; (b) LMs do not reason in an abstract manner and are context-dependent, e.g., while RoBERTa can compare ages, it can do so only when the ages are in the typical range of human ages; (c) On half of our reasoning tasks all models fail completely. Our findings and infrastructure can help future work on designing new datasets, models, and objective functions for pre-training.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}


<hr class="thin" />
{: .fs-4 .fw-800 .text-blue-100}
**📜 Evaluating Commonsense in Pre-trained Language Models**. <br> ✍ Xuhui Zhou, Y. Zhang, Leyang Cui, Dandan Huang *(AAAI 2020)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/pdf/1911.11931.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/XuhuiZhou/CATS){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Evaluating-Commonsense-in-Pre-trained-Language-Zhou-Zhang/9399b0f7a7dfb7b3497fbd91d0bf6542513b0904){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [Sense Making](https://github.com/wangcunxiang/Sen-Making-and-Explanation){: .mr-1 target="_blank"}, [WSC](/docs/datasets#wsc){: .mr-1 target="_blank"}, [SWAG](/docs/datasets#swag-and-hellaswag){: .mr-1 target="_blank"}, [HellaSwag](/docs/datasets#swag-and-hellaswag){: .mr-1 target="_blank"},[Argument Reasoning Comprehension](https://github.com/UKPLab/argument-reasoning-comprehension-task){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Contextualized representations trained over large raw text data have given remarkable improvements for NLP tasks including question answering and reading comprehension. There have been works showing that syntactic, semantic and word sense knowledge are contained in such representations, which explains why they benefit such tasks. However, relatively little work has been done investigating commonsense knowledge contained in contextualized representations, which is crucial for human question answering and reading comprehension. We study the commonsense ability of GPT, BERT, XLNet, and RoBERTa by testing them on seven challenging benchmarks, finding that language modeling and its variants are effective objectives for promoting models' commonsense ability while bi-directional context and larger training set are bonuses. We additionally find that current models do poorly on tasks require more necessary inference steps. Finally, we test the robustness of models by making dual test cases, which are correlated so that the correct prediction of one sample should lead to correct prediction of the other. Interestingly, the models show confusion on these test cases, which suggests that they learn commonsense at the surface rather than the deep level. We release a test set, named CATs publicly, for future research.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}

 

<hr class="thin" />
{: .fs-4 .fw-800 .text-blue-100}
**📜 RICA: Evaluating Robust Inference Capabilities Based on Commonsense Axioms**. <br> ✍ Pei Zhou, Rahul Khanna, Seyeon Lee, Bill Yuchen Lin, Daniel Ho, Jay Pujara, Xiang Ren *(arXiv 2020, accepted in EMNLP-Findings 2020)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/pdf/2005.00782.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Project Page](https://sites.google.com/usc.edu/rica){: target="_blank" .btn .btn-green .mr-1 } 
   [Leaderboard](https://eval.ai/web/challenges/challenge-page/832/overview){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/RICA%3A-Evaluating-Robust-Inference-Capabilities-on-Zhou-Khanna/4f1312c6c2fbc831652c099ea4ddbd1e1ad67c59){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [ConceptNet](https://conceptnet.io/){: .mr-1 target="_blank"},[ATOMIC](https://mosaickg.apps.allenai.org/kg_atomic){: .mr-1 target="_blank"}, [COMeT](https://mosaickg.apps.allenai.org/comet_atomic){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Pre-trained language models (PTLM) have impressive performance on commonsense inference benchmarks, but their ability to practically employ commonsense to communicate with humans is fiercely debated. Prior evaluations of PTLMs have focused on factual world knowledge or the ability to reason when the necessary knowledge is provided explicitly. However, effective communication with humans requires inferences based on implicit commonsense relationships, and robustness despite paraphrasing. In the pursuit of advancing fluid human-AI communication, we propose a new challenge, RICA, that evaluates the capabilities of making commonsense inferences and the robustness of these inferences to language variations. In our work, we develop a systematic procedure to probe PTLMs across three different evaluation settings. Extensive experiments on our generated probe sets show that PTLMs perform no better than random guessing (even with fine-tuning), are heavily impacted by statistical biases, and are not robust to perturbation attacks. Our framework and probe sets can help future work improve PTLMs' inference abilities and robustness to linguistic variations--bringing us closer to more fluid communication. 
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}




---

## Analyzing Reasoning Methods

|<span class="fs-4">The following papers focus on how the existing methods perform their reasoning for commonsense tasks. </span>|


{: .fs-4 .fw-800 .text-blue-100}
**📜 Does BERT Solve Commonsense Task via Commonsense Knowledge?**. <br> ✍ Leyang Cui, Sijie Cheng, Yu Wu, Yue Zhang *(AAAI 2020)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/pdf/2008.03945.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Does-BERT-Solve-Commonsense-Task-via-Commonsense-Cui-Cheng/d8ea988072efb115ee8c85e159c1fa4a816360b5){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [ConceptNet](https://conceptnet.io/){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  The success of pre-trained contextualized language models such as BERT motivates a line of work that investigates linguistic knowledge inside such models in order to explain the huge improvement in downstream tasks. While previous work shows syntactic, semantic and word sense knowledge in BERT, little work has been done on investigating how BERT solves CommonsenseQA tasks. In particular, it is an interesting research question whether BERT relies on shallow syntactic patterns or deeper commonsense knowledge for disambiguation. We propose two attention-based methods to analyze commonsense knowledge inside BERT, and the contribution of such knowledge for the model prediction. We find that attention heads successfully capture the structured commonsense knowledge encoded in ConceptNet, which helps BERT solve commonsense tasks directly. Fine-tuning further makes BERT learn to use the commonsense knowledge on higher layers.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}


<hr class="thin" />
{: .fs-4 .fw-800 .text-blue-100}
**📜 Learning to Deceive Knowledge Graph Augmented Models via Targeted Perturbation**. <br> ✍ Mrigank Raman, Siddhant Agarwal, Peifeng Wang, Aaron Chan, H. Wang, Sungchul Kim, Ryan A. Rossi, Handong Zhao, Nedim Lipka, Xiang Ren *(ICLR 2021)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/pdf/2010.12872.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/INK-USC/deceive-KG-models){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Learning-to-Deceive-Knowledge-Graph-Augmented-via-Raman-Agarwal/a5654d5244b908a08936fcb7c13c03124dd5648e){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [CommonsenseQA](/docs/datasets#commonsenseqa){: .mr-1 target="_blank"}, [ConceptNet](https://conceptnet.io/){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Knowledge graphs (KGs) have helped neural-symbolic models improve performance on various knowledge-intensive tasks, like question answering and item recommendation. By using attention over the KG, such models can also "explain" which KG information was most relevant for making a given prediction. In this paper, we question whether these models are really behaving as we expect. We demonstrate that, through a reinforcement learning policy (or even simple heuristics), one can produce deceptively perturbed KGs which maintain the downstream performance of the original KG while significantly deviating from the original semantics and structure. Our findings raise doubts about KG-augmented models' ability to leverage KG information and provide plausible explanations
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}



---

## Analysis on Data

| <span class="fs-4">These papers work on analyzing the datasets and resources we used for studying commonsense reasoning. Are they biased? Do they contain error or noise? Why are the real challenges? </span>|

{: .fs-4 .fw-800 .text-blue-100}
**📜 Lawyers are Dishonest? Quantifying Representational Harms in Commonsense Knowledge Resources**. <br> ✍ 
Ninareh Mehrabi\*, Pei Zhou\*, Fred Morstatter, Jay Pujara, Xiang Ren, Aram Galstyan *(arXiv 2021)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/pdf/2103.11320.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/Ninarehm/Commonsense_bias){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Lawyers-are-Dishonest-Quantifying-Representational-Mehrabi-Zhou/f54497893ee8e7dc888d062bc5498dcb2791f525){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [ConceptNet](https://conceptnet.io/){: .mr-1 target="_blank"}, [COMeT](https://mosaickg.apps.allenai.org/comet_atomic){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Numerous natural language processing models have tried injecting commonsense by using the ConceptNet knowledge base to improve performance on different tasks. ConceptNet, however, is mostly crowdsourced from humans and may reflect human biases such as “lawyers are dishonest.” It is important that these biases are not conflated with the notion of commonsense. We study this missing yet important problem by first defining and quantifying biases in ConceptNet as two types of representational harms: overgeneralization of polarized perceptions and representation disparity. We find that ConceptNet contains severe biases and disparities across four demographic categories. In addition, we analyze two downstream models that use ConceptNet as a source for commonsense knowledge and find the existence of biases in those models as well. We further propose a filtered-based bias-mitigation approach and examine its effectiveness. We show that our mitigation approach can reduce the issues in both resource and models but leads to a performance drop, leaving room for future work to build fairer and stronger commonsense models.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}




<hr class="thin" />
{: .fs-4 .fw-800 .text-blue-100}
**📜 WinoWhy: A Deep Diagnosis of Essential Commonsense Knowledge for Answering Winograd Schema Challenge**. <br> ✍ Hongming Zhang\*, Xinran Zhao\*, Yangqiu Song *(ACL 2020)*
 
<span class="fs-2">
   [Paper](https://www.aclweb.org/anthology/2020.acl-main.508.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/HKUST-KnowComp/WinoWhy){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/WinoWhy%3A-A-Deep-Diagnosis-of-Essential-Commonsense-Zhang-Zhao/827ac6fd6bd5a0a7607085c10e27641a60b5e4fe){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [WSC](/docs/datasets#wsc){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  In this paper, we present the first comprehensive categorization of essential commonsense knowledge for answering the Winograd Schema Challenge (WSC). For each of the questions, we invite annotators to first provide reasons for making correct decisions and then categorize them into six major knowledge categories. By doing so, we better understand the limitation of existing methods (i.e., what kind of knowledge cannot be effectively represented or inferred with existing methods) and shed some light on the commonsense knowledge that we need to acquire in the future for better commonsense reasoning. Moreover, to investigate whether current WSC models can understand the commonsense or they simply solve the WSC questions based on the statistical bias of the dataset, we leverage the collected reasons to develop a new task called WinoWhy, which requires models to distinguish plausible reasons from very similar but wrong reasons for all WSC questions. Experimental results prove that even though pre-trained language representation models have achieved promising progress on the original WSC dataset, they are still struggling at WinoWhy. Further experiments show that even though supervised models can achieve better performance, the performance of these models can be sensitive to the dataset distribution. WinoWhy and all codes are available at: this https URL
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}


<hr class="thin" />
{: .fs-4 .fw-800 .text-blue-100}
**📜 Commonsense Knowledge Graph Reasoning by Selection or Generation? Why?**. <br> ✍ Cunxiang Wang, Jinhang Wu, Luxin Liu, Yue Zhang *(arXiv 2020)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/pdf/2008.05925.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Commonsense-Knowledge-Graph-Reasoning-by-Selection-Wang-Wu/6d8ee95a87f756e03327888bd4318ee108f4c715){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [ConceptNet](https://conceptnet.io/){: .mr-1 target="_blank"}, [ATOMIC](https://mosaickg.apps.allenai.org/kg_atomic){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Commonsense knowledge graph reasoning(CKGR) is the task of predicting a missing entity given one existing and the relation in a commonsense knowledge graph (CKG). Existing methods can be classified into two categories generation method and selection method. Each method has its own advantage. We theoretically and empirically compare the two methods, finding the selection method is more suitable than the generation method in CKGR. Given the observation, we further combine the structure of neural Text Encoder and Knowledge Graph Embedding models to solve the selection method's two problems, achieving competitive results. We provide a basic framework and baseline model for subsequent CKGR tasks by selection methods.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}


<hr class="thin" />
{: .fs-4 .fw-800 .text-blue-100}
**📜 An Analysis of Dataset Overlap on Winograd-Style Tasks**. <br> ✍ Ali Emami, Adam Trischler, Kaheer Suleman, Jackie Chi Kit Cheung *(COLING 2020)*
 
<span class="fs-2">
   [Paper](https://www.aclweb.org/anthology/2020.coling-main.515.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/aemami1/KnowRef60k){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/An-Analysis-of-Dataset-Overlap-on-Winograd-Style-Emami-Trischler/16992445d3114d27fb64d2d00cd35b421bef7930){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** [WSC](/docs/datasets#wsc){: .mr-1 target="_blank"}
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
 The Winograd Schema Challenge (WSC) and variants inspired by it have become important benchmarks for common-sense reasoning (CSR). Model performance on the WSC has quickly progressed from chance-level to near-human using neural language models trained on massive corpora. In this paper, we analyze the effects of varying degrees of overlap between these training corpora and the test instances in WSC-style tasks. We find that a large number of test instances overlap considerably with the corpora on which state-of-the-art models are (pre)trained, and that a significant drop in classification accuracy occurs when we evaluate models on instances with minimal overlap. Based on these results, we develop the KnowRef-60K dataset, which consists of over 60k pronoun disambiguation problems scraped from web data. KnowRef-60K is the largest corpus to date for WSC-style common-sense reasoning and exhibits a significantly lower proportion of overlaps with current pretraining corpora.
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}


---

## Others
 
{: .fs-4 .fw-800 .text-blue-100}
**📜 The Box is in the Pen: Evaluating Commonsense Reasoning in Neural Machine Translation**. <br> ✍ Jie He, Tao Wang, Deyi Xiong, Qun Liu *(EMNLP-Findings 2020)*
 
<span class="fs-2">
   [Paper](https://arxiv.org/pdf/2103.11320.pdf){: .btn .btn-blue .mr-1 target="_blank" } 
   [Code](https://github.com/Ninarehm/Commonsense_bias){: target="_blank" .btn .btn-green .mr-1 } 
   [Semantic Scholar](https://www.semanticscholar.org/paper/Lawyers-are-Dishonest-Quantifying-Representational-Mehrabi-Zhou/f54497893ee8e7dc888d062bc5498dcb2791f525){: .btn .btn-purple .mr-1 target="_blank" }
</span> 

**Used Resources:** 
<details markdown="block">
  <summary>Abstract</summary>
  {: .fs-3 .text-delta .text-blue-100}
  ```
  Does neural machine translation yield translations that are congenial with common sense? In this paper, we present a test suite to evaluate the commonsense reasoning capability of neural machine translation. The test suite consists of three test sets, covering lexical and contextless/contextual syntactic ambiguity that requires commonsense knowledge to resolve. We manually create 1,200 triples, each of which contain a source sentence and two contrastive translations, involving 7 different common sense types. Language models pretrained on large-scale corpora, such as BERT, GPT-2, achieve a commonsense reasoning accuracy of lower than 72% on target translations of this test suite. We conduct extensive experiments on the test suite to evaluate commonsense reasoning in neural machine translation and investigate factors that have impact on this capability. Our experiments and analyses demonstrate that neural machine translation performs poorly on commonsense reasoning of the three ambiguity types in terms of both reasoning accuracy ( 6 60.1%) and reasoning consistency (6 31%). We will release our test suite as a machine translation commonsense reasoning testbed to promote future work in this direction
  ``` 
  <!-- ![Machine Common Sense](/images/asimplemethod.png){: width="700" text-align="center"} -->
</details> 
{: .fs-5 .fw-600 .text-blue-300}

<details markdown="block">
  <summary>Comments</summary>
  {: .fs-3 .text-delta .text-red-100}
</details> 
{: .fs-3 .fw-600 .text-red-300}



<!-- 1. RICA's related works. + LAMA probes + olymics + Yue Zhang's papers (two)  -->
<!-- (1 Yue) Evaluating commonsense in pre-trained language models from Yue Zhang -->
<!-- (2 Yue) Does BERT Solve Commonsense Task via Commonsense Knowledge?  https://www.semanticscholar.org/paper/Does-BERT-Solve-Commonsense-Task-via-Commonsense-Cui-Cheng/d8ea988072efb115ee8c85e159c1fa4a816360b5 -->
<!-- 2. ICLR 2021 paper on KG faithfulness -->
<!-- 3. Pei's new arxiv on bias in KG -->
<!-- 4. The Box is in the Pen: Evaluating Commonsense Reasoning in Neural Machine Translation. -->
<!-- 5. WinoWhy: A Deep Diagnosis of Essential Commonsense Knowledge for Answering Winograd Schema Challenge -->
<!-- 6. Commonsense Knowledge Graph Reasoning by Selection or Generation? Why? -->
<!-- 7. An Analysis of Dataset Overlap on Winograd-Style Tasks (COLING 2020) -->
