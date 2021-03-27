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

Editors: [Bill Yuchen Lin](https://yuchenlin.xyz/), [Yang Qiao](https://www.linkedin.com/in/xiaoyang-qiao/)

{: .fs-5 .fw-300 }

We present a comprehensive collection of datasets for testing commonsense reasoning ability. They are gourped by different fomulations, and covered a wide range of aspects: properties of common objects, real-life situations, elementry science, social skills, etc. 

| Name | Focus | Format |  SotA vs. Human  | \# Citations |
| :------------:| :-----: | :------: | :----------: | :-------: | :-----------: | :------------: |
| [CommonsenseQA](#commonsenseqa) | General | [MCQA](#Multiple-Choice-QA)  | [83.3]() /  88.9 (**Acc. %**)  | 174 |
| [SocialIQA](#socialiqa) | Social Interactions | [MCQA](#Multiple-Choice-QA)  | [83.15]() /  88.1 (**Acc. %**)  | 90 |
| [PhysicalIQA](#physicaliqa) | General | [MCQA](#Multiple-Choice-QA)  | [90.13]() /  94.9 (**Acc. %**)  | 43 |
| [ARC](#arc) | Science | [MCQA](#Multiple-Choice-QA)  | [81.4]() /  unknown (**Acc. %**)  | 177 |
| [OpenbookQA](#openbookqa) | General | [MCQA](#Multiple-Choice-QA)  | [87.2]() /  91.7 (**Acc. %**)  | 125 |
| [SWAG](#swag-and-hellaswag) | General | [MCQA](#Multiple-Choice-QA)  | [91.71]() /  88 (**Acc. %**)  | 281 |
| [HellaSWAG](#swag-and-hellaswag) | General | [MCQA](#Multiple-Choice-QA)  | [93.85]() /  95.6 (**Acc. %**)  | 107 |
| [WSC](#wsc) | General | [MCQA](#Multiple-Choice-QA)  |  |  |
| [WinoGrande](#winogrande) | General | [MCQA](#Multiple-Choice-QA)  | [91.28]() /  94 (**Acc. %**)  | 108 |
| [COPA](#copa-and-x-copa) | General | [MCQA](#Multiple-Choice-QA)  |  | 17 |
| [X-COPA](#copa-and-x-copa) | General | [MCQA](#Multiple-Choice-QA)  |  | 9 |
| [CODAH](#codah) | General | [MCQA](#Multiple-Choice-QA)  |  | 5 |
| [MC-TACO](#mc-taco) | Temporal Commonsense | [MCQA](#Multiple-Choice-QA)  | [80.87]() /  75.8 (**Acc. %**)  | 25 |
| [aNLI](#anli) | General | [MCQA](#Multiple-Choice-QA)  | [89.7]() /  92.9 (**Acc. %**)  | 62 |
| [RiddleSense](#riddlesense) | General | [MCQA](#Multiple-Choice-QA)  |  |  |


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

{: .fs-4 .fw-800 .text-blue-100}
*SocialIQA: Commonsense Reasoning about Social Interactions*. Maarten Sap, Hannah Rashkin, Derek Chen, Ronan Le Bras, Yejin Choi. **EMNLP-19**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1904.09728){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://leaderboard.allenai.org/socialiqa/submissions/get-started){: target="_blank" .btn .btn-green .mr-1 } </span>

> - **Topics:** Social Interactions. It focuses on reasoning about people’s actions and their social implications.
- **Size & Split:**  37,588 in total --- train (33,410), dev (1,954), test (2,224).
- **Data generation:** 
- **An illustative example:**
```
Question: 
    In the school play, Robin played a hero in the struggle to the death with the angry villain. How would others feel as a result?
Choices:  
    A) sorry for the villain
    B) hopeful that Robin will succeed
    C) like Robin should lose the fight
Correct Choice: B
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### PhysicalIQA
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*PIQA: Reasoning about Physical Commonsense in Natural Language*. Yonatan Bisk, Rowan Zellers, Ronan Le Bras, Jianfeng Gao, Yejin Choi. **AAAI-20**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1911.11641){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://leaderboard.allenai.org/physicaliqa/submissions/get-started){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/piqa){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. It focuses on how people interact with everyday objects in everyday situations.
- **Size & Split:**  around 20,000 QA pairs of multiple-choice in total --- train (over 16,000), dev (∼2K), test (∼3k).
- **Data generation:** 
- **An illustative example:**
```
Question:
    To separate egg whites from the yolk using a water bottle, you should
Choices:
    A) Squeeze the water bottle and press it against the yolk. Release, which creates suction and lifts the yolk.
    B) Place the water bottle and press it against the yolk. Keep pushing, which creates suction and lifts the yolk.
Correct Choice: B
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### ARC 
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*Think you have Solved Question Answering? Try ARC, the AI2 Reasoning Challenge*. Peter Clark, Isaac Cowhey, Oren Etzioni, Tushar Khot, Ashish Sabharwal, Carissa Schoenick, Oyvind Tafjord. **unknown**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1803.05457){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://leaderboard.allenai.org/arc/submissions/get-started){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/ai2_arc){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** Science. It focuses on natural, grade-school science questions.
- **Size & Split:**  7,787 in total --- train (3,370), dev (869), test (3,548).
- **Data generation:** 
- **An illustative example:**
```
Question:
    Which property of a mineral can be determined just by looking at it?
Choices:
    A) luster  B) mass  C) weight  D) hardness
Correct Choice: A
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### OpenbookQA
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*Can a Suit of Armor Conduct Electricity? A New Dataset for Open Book Question Answering*. Todor Mihaylov, Peter Clark, Tushar Khot, Ashish Sabharwal. **EMNLP-18**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1809.02789){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://leaderboard.allenai.org/open_book_qa/submissions/get-started){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/openbookqa){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. The dataset is modeled after open book exams for assessing human understanding of a subject.
- **Size & Split:**  5,957 in total --- train (4,957), dev (500), test (500).
- **Data generation:** 
- **An illustative example:**
```
Question:
    Which of these would let the most heat travel through?
Choices:
    A) a new pair of jeans
    B) a steel spoon in a cafeteria  
    C) a cotton candy at a store  
    D) a calvi klein cotton hat
Correct Choice: B
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->


### SWAG and HellaSWAG
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*SWAG: A Large-Scale Adversarial Dataset for Grounded Commonsense Inference*. Rowan Zellers, Yonatan Bisk, Roy Schwartz, Yejin Choi. **EMNLP-18**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1808.05326){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://rowanzellers.com/swag/){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/swag){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. Mostly about grounded situations. Each question is a video caption from LSMDC or ActivityNet Captions, with four answer choices about what might happen next in the scene. 
- **Size & Split:**  around 113k in total --- train (73k), dev (20k), test (20k).
- **Data generation:** 
- **An illustative example:**
```
Question:
    On stage, a woman takes a seat at the piano. She
Choices:
    A) sits on a bench as her sister plays with the doll.
    B) smiles with someone as the music plays.
    C) is in the crowd, watching the dancers.
    D) nervously sets her fingers on the keys.
Correct Choice: D
``` 

{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->


{: .fs-4 .fw-800 .text-blue-100}
*HellaSwag: Can a Machine Really Finish Your Sentence?*. Rowan Zellers, Ari Holtzman, Yonatan Bisk, Ali Farhadi, Yejin Choi. **ACL-19**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1905.07830){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://rowanzellers.com/hellaswag/){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/hellaswag){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. Mostly about grounded commonsense situations.
- **Size & Split:**  18,001 in total --- train (6,833), dev (3,641), test (7,527).
- **Data generation:** 
- **An illustative example:**
```
Question:
    A woman is outside with a bucket and a dog. The dog is running around trying to avoid a bath. She
Choices:
    A) rinses the bucket off with soap and blow dries the dog's head.
    B) uses a hose to keep it from getting soapy.
    C) gets the dog wet, then it runs away again.
    D) gets into the bath tub with the dog.
Correct Choice: C
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->


### WSC 
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*The Winograd Schema Challenge*. Ernest Davis, Leora Morgenstern, and Charles Ortiz. **unknown**

<span class="fs-1">
[Paper](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.729.9814&rep=rep1&type=pdf){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://cs.nyu.edu/faculty/davise/papers/WinogradSchemas/WS.html){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/winograd_wsc){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. 
- **Size & Split:**  xxx in total --- train (xxx), dev (xxx), test (xxx).
- **Data generation:** 
- **An illustative example:**
```
label: 0,
options: ['The city councilmen', 'The demonstrators']
pronoun: they
pronoun_loc: 63
quote: they feared violence
quote_loc: 63
source: (Winograd 1972)
text: The city councilmen refused the demonstrators a permit because they feared violence.
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### WinoGrande
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*WinoGrande: An Adversarial Winograd Schema Challenge at Scale*. Keisuke Sakaguchi, Ronan Le Bras, Chandra Bhagavatula, Yejin Choi. **unknown**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1907.10641){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://winogrande.allenai.org/){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/winogrande){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. Mostly about commonsense inference in pronoun resolution problems.
- **Size & Split:**  43,972 in total --- train (40,938), dev (1,267), test (1,767).
- **Data generation:** 
- **An illustative example:**
```
Sentence: Katrina had the financial means to afford a new car while Monica did not, since _ had a high paying job.
Option1: Katrina
Option2: Monica
Correct Option: Option1
``` 

{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### COPA and X-COPA 
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*Choice of Plausible Alternatives: An Evaluation of Commonsense Causal Reasoning*. Melissa Roemmele, Cosmin Adrian Bejan, and Andrew S. Gordon. **AAAI-11**

<span class="fs-1">
[Paper](https://www.researchgate.net/publication/221251392_Choice_of_Plausible_Alternatives_An_Evaluation_of_Commonsense_Causal_Reasoning){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://people.ict.usc.edu/~gordon/copa.html){: target="_blank" .btn .btn-green .mr-1 } </span>

> - **Topics:** General. Open-domain commonsense causal reasoning of everyday activities.
- **Size & Split:**  1000 in total --- dev (500), test (500).
- **Data generation:** 
- **An illustative example:**
```
Premise: The man broke his toe. What was the CAUSE of this?
Alternative 1: He got a hole in his sock.
Alternative 2: He dropped a hammer on his foot.
Correct Choice: Alternative 2
``` 

{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->


{: .fs-4 .fw-800 .text-blue-100}
*XCOPA: A Multilingual Dataset for Causal Commonsense Reasoning*. Edoardo Maria Ponti, Goran Glavaš, Olga Majewska, Qianchu Liu, Ivan Vulić, Anna Korhonen. **unknown**

<span class="fs-1">
[Paper](https://arxiv.org/abs/2005.00333){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://github.com/cambridgeltl/xcopa){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/xcopa){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. Same as COPA dataset but in 11 languages.
- **Size & Split:**  1000 * 11(lang) in total --- dev (500 * 11), test (500 * 11).
- **Data generation:** 
- **An illustative example (in Italian):**
```
Premise: L'uomo aprì il rubinetto.
Alternative 1: Il gabinetto si riempì d'acqua.
Alternative 2: Dell'acqua fluì dal beccuccio.
Correct Choice: Alternative 1
``` 

{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### CODAH 
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*CODAH: An Adversarially Authored Question-Answer Dataset for Common Sense*. Michael Chen, Mike D'Arcy, Alisa Liu, Jared Fernandez, Doug Downey. **RepEval-19**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1904.04365){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://github.com/Websail-NU/CODAH){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/codah){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. Mostly about grounded situations in everyday activities. 
- **Size:**  2,801 in total.
- **Data generation:** 
- **An illustative example:**
```
Question: 
    I am always very hungry before I go to bed. I am
Choices:
    A) concerned that this is an illness.
    B) glad that I do not have a kitchen.
    C) fearful that there are monsters under my bed.
    D) tempted to snack when I feel this way.
Correct Choice: D
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### MC-TACO
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*"Going on a vacation" takes longer than "Going for a walk": A Study of Temporal Commonsense Understanding*. Ben Zhou, Daniel Khashabi, Qiang Ning, Dan Roth. **EMNLP-19**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1909.03065){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://leaderboard.allenai.org/mctaco/submissions/get-started){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/mc_taco){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** Temporal Commonsense. Focusing on event ordering, duration, stationarity, frequency and time.
- **Size & Split:**  13k question-answer pairs in total --- dev (3,783), test (9,442) .
- **Data generation:** 
- **An illustative example:**
```
Paragraph: 
    Growing up on a farm near St. Paul, L. Mark Bailey didn't dream of becoming a judge.
Question:
    How many years did it take for Mark to become a judge?
Choices:
    A) 63 years  B) 7 weeks  C) 7 years  D) 7 seconds  E) 7 hours
Correct Choice: C
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->


### aNLI
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*Abductive Commonsense Reasoning*. Chandra Bhagavatula, Ronan Le Bras, Chaitanya Malaviya, Keisuke Sakaguchi, Ari Holtzman, Hannah Rashkin, Doug Downey, Scott Wen-tau Yih, Yejin Choi. **ICLR-20**

<span class="fs-1">
[Paper](https://arxiv.org/abs/1908.05739){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://leaderboard.allenai.org/anli/submissions/get-started){: target="_blank" .btn .btn-green .mr-1 }, [Huggingface Card](https://huggingface.co/datasets/art){: target="_blank" .btn .btn-purple .mr-1 } </span>

> - **Topics:** General. Mostly about observations of objects or events in daily life.
- **Size & Split:**  17,801 context pairs in total --- dev (1,532), test (3,059).
- **Data generation:** 
- **An illustative example:**
```
Obs1: It was a gorgeous day outside.
Obs2: She asked her neighbor for a jump-start.
Hyp1: Mary decided to drive to the beach, but her car would not start due to a dead battery.
Hyp2: It made a weird sound upon starting.
Correct Choice: Hyp1
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->



### RiddleSense
{: .no_toc }

{: .fs-4 .fw-800 .text-blue-100}
*RiddleSense: Answering Riddle Questions as Commonsense Reasoning*. Bill Yuchen Lin, Ziyi Wu, Yichi Yang, Dong-Ho Lee, Xiang Ren.

<span class="fs-1">
[Paper](https://arxiv.org/abs/2101.00376){: .btn .btn-blue .mr-1 target="_blank" }, [Official Link](https://inklab.usc.edu/RiddleSense/){: target="_blank" .btn .btn-green .mr-1 } </span>

> - **Topics:** General. Mostly about riddle-style commonsense question answering.
- **Size & Split:**  5,733 in total --- train (3,510), dev (1,021), test (1,202).
- **Data generation:** 
- **An illustative example:**
```
Question:
    My life can be measured in hours. I serve by being devoured. Thin, I am quick; Fat, I am slow. Wind is my foe. What am I?
Choices:
    A) paper  B) candle  C) lamp  D) 7  clock  E) worm
Correct Choice: B
``` 


{: .fs-4 .fw-600 .text-red-300}
> **Editors' comments**

<!-- Mention the highlights or known issues of the dataset. -->




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

### ReCoRD
{: .no_toc }

### Cosmos QA
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

### GLUE and SuperGLUE Benchmark 
{: .no_toc }

<!-- https://super.gluebenchmark.com/tasks -->