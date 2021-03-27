---
layout: default
title: Benchmark Datasets
nav_order: 3
toc_list: true
last_modified_date: March 26 2021
permalink: /docs/datasets
---

# Benchmark Datasets for Commonsense Reasoning
{: .no_toc }

Editors: [Bill Yuchen Lin](https://yuchenlin.xyz/), 

{: .fs-5 .fw-300 }

We present a comprehensive collection of datasets that are designed for testing commonsense reasoning ability. They are gourped by their fomulations, while they covered a wide range of aspects: properties of common objects, real-life situations, elementry science, social skills, etc. 

---

Below is a table for summarizing the infomation 

| Name | Focus | Format |  SotA vs. Human  | \# Citations |
| :------------:| :-----: | :------: | :----------: | :-------: | :-----------: | :------------: |
| [CommonsenseQA](#commonsenseqa) | General | [Multiple-Choice](#Multiple-Choice-QA)  | [83.3]() /  88.9 (**Acc. %**)  | 174 |

<!-- Check https://leaderboard.allenai.org/ for more -->

---

## Multiple-Choice QA

<!-- You can use this google sheet: https://docs.google.com/spreadsheets/d/1vJUwjFA_HRvzRI3ULSWXS7rLbHriJj5bTYSUiG4Iixo/edit?usp=sharing 
 and then conver it to markdown by https://tabletomarkdown.com/convert-spreadsheet-to-markdown/ -->
 

The task format for multiple-choice question answering (**MCQA**) is as follows.
- Input: a question, a few candidate answers (i.e., choices).
- Output: the label of the correct choice. 
- Metric: accuracy. 

Notes:
- There is **one and only one correct choice** for each input, and the others are distractors.
- We do not consider the cases with additional input context (e.g., [passages](#CosmosQA), [images](#visual-commonsense-reasoning)) here.
- The inputs can be either __interrogative questions__ (as in CommonsenseQA, SocialIQA, etc.) or __incomplete statements__ (as in SWAG, COPA, WSC, etc.).

 
### CommonsenseQA
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*CommonsenseQA: A Question Answering Challenge Targeting Commonsense Knowledge*. Alon Talmor, Jonathan Herzig, Nicholas Lourie, Jonathan Berant. **NAACL-19**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1811.00937){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://www.tau-nlp.org/commonsenseqa){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/commonsense_qa){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. Mostly about properties of common objects and motivation/causes/results of events.
- **Size & Split:** 12,102 in total --- train (9,741), dev (1,221), test (1,140).
- **Data generation:** The questions are crowdsourced from human annotators. The authors present a question concept, _q_, and some candidate concepts, which are linked to _q_, and ask annotators to write a natural-language question mentioning _q_ and answered by only one of the answer candidates.
- **An illustative example:**
```
Question ID: b8c0a4703079cf661d7261a60a1bcbff
Question concept: "magazines"
Question: "Where would you find magazines along side many other printed works?"
Choices:  A: "doctor" | B: "bookstore" | C: "market" | D: "train station" | E: "mortuary"
Correct Choice: B
``` 



{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->


> - We use the latest version of the data (v1.11) downloaded from the official website to report the size, which is thus different from the paper.




### SocialIQA 
{: .no_toc }


### PhysicalIQA
{: .no_toc }


### ARC 
{: .no_toc }

### OpenbookQA
{: .no_toc }


### SWAG and HellaSWAG
{: .no_toc }

### WSC 
{: .no_toc }

### WinoGrande
{: .no_toc }


### COPA and X-COPA 
{: .no_toc }



### CODAH 
{: .no_toc }


### MC-TACO
{: .no_toc }


### RiddleSense
{: .no_toc }



---

## Visually-Grounded QA

### Visual Commonsense Reasoning
{: .no_toc }
 <!-- https://visualcommonsense.com/ -->

---



## Open-Ended QA

### ProtoQA
{: .no_toc }

### OpenCSR
{: .no_toc }


---

## Constrained NLG

### CommonGen
{: .no_toc }


---


## LM Probing Tasks

### LAMA Probes 
{: .no_toc }

### NumerSense
{: .no_toc }

---

## Reading Comprehension 

### ReCORD
{: .no_toc }

### CosmosQA
{: .no_toc }


---


## Text Game

### TWC
{: .no_toc }

### AFLWorld
{: .no_toc }

---



## Other Related Datasets


### LocatedNear Relation Extraction
{: .no_toc }

### SNLI and MNLI
{: .no_toc }

