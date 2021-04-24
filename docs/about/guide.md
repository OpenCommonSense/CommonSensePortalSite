---
layout: default
title: Guide
nav_order: 2
has_children: False
permalink: /about/

toc_list: true
last_modified_date: March 23 2021
---



# A Gentle Introduction to Commonsense Reasoning
{: .no_toc }

Editors: [Bill Yuchen Lin](https://yuchenlin.xyz/), ...


<style>
td{
    font-size: 15pt;
}
</style>

## What is commonsense reasoning?

In general, commonsense reasoning is the ability to make decisions in *real-world situations* with the knowledge shared by most people. 
Commonsense reasoning is hard to define, particularly due to the ambiguous boundary of commonsense knowledge. 
In the following, we show some definitions and characterizations of common sense from different authors, and finally give a summary as **[our working definition]()**.


<table>
<td markdown="block" class="fs-4">
In artificial intelligence (AI), **commonsense reasoning is a human-like ability to make presumptions about the type and essence of ordinary situations humans encounter every day**. 
These assumptions include judgments about the nature of physical objects, taxonomic properties, and peoples' intentions. 
A device that exhibits commonsense reasoning might be capable of drawing conclusions that are similar to humans' **folk psychology** (i.e., *humans' innate ability to reason about people's behavior and intentions*) and **naive physics** (i.e., *humans' natural understanding of the physical world*). Below are some existing definitions of commonsense knowledge.

1. "Commonsense knowledge includes the basic facts about *events* (including actions) and their *effects*, facts about knowledge and how it is obtained, facts about beliefs and desires. It also includes the basic facts about material *objects* and their *properties*." ([McCarthy, John; 1989]())
1. "Commonsense knowledge **differs from *encyclopedic* knowledge** in that it deals with *general* knowledge rather than the details of specific entities." ([Tandon et al. 2018](https://dl.acm.org/doi/10.1145/3186549.3186562))
1. Commonsense knowledge is "real world knowledge that can **provide a *basis*** for additional knowledge to be gathered and interpreted automatically". ([Matuszek, Cynthia, et al. 2005]())
1. The commonsense world consists of "**time, space, physical interactions, people,** and so on". ([Ernest Davis; Gary Marcus 2015](https://www.aaai.org/Library/AAAI/2005/aaai05-227.php))
1. Common sense is "all the knowledge about the world that we **take for *granted* but *rarely state*** out loud". ([Clive Thompson 2020](https://www.wired.com/story/how-to-teach-artificial-intelligence-common-sense/))
<!-- 1. Common sense is "broadly reusable background knowledge that's not specific to a particular subject area... knowledge that you ought to have." ([Pavlus, John; 2020](https://www.quantamagazine.org/common-sense-comes-to-computers-20200430/)) -->
<!-- 1. Commonsense knowledge is "what a typical seven year old knows about the world", including physical objects, substances, plants, animals, and human society". ([Davis, Ernest 2017](https://doi.org/10.1613%2Fjair.5339)) -->

{: style="text-align:right; margin-bottom:0.1em" .fs-2}
--- **(Modified) Wikipedia: [Commonsense Reasoning](https://en.wikipedia.org/wiki/Commonsense_reasoning){: target="_blank"}**
</td>
</table>


<table>
<td markdown="block" class="fs-4">

Common sense is the *basic* level of practical knowledge and reasoning concerning **situations and events** that are commonly shared among most people. Commonsense knowledge can be categorized according to types, including but not limited to:


- **Physical common sense:** Physical common sense includes knowledge about the physical **properties** and **affordances** of everyday objects. 
<!-- For example, a glass will likely shatter if it falls to the floor, is a fact most people know.  -->


- **Social common sense:** People are capable of making inferences about other people's **mental states**, e.g. what *motivates* them, what they are *likely to do next*, etc. In addition, we each have a set of **social norms** of accepted behavior. These are often *implicit* in our actions and decisions. 

- **Temporal common sense:** natural language rarely communicates explicit temporal information. Instead it's vague and relies on the commonsense knowledge of the listener. 
<!-- For example, when told that "Dr. Porter is taking a vacation" we can predict that Dr. Porter will not be able to see us soon, as opposed to when "Dr. Porter is taking a walk".  -->
This requires knowing the **typical duration**, **times, order, frequency, etc. of events**.
<!-- "taking a walk" (minutes) and that of "taking a vacation" (days). Other temporal knowledge is  -->
 
{: style="text-align:right; margin-bottom:0.1em" .fs-2}
--- **(Modified) A [blog post](http://veredshwartz.blogspot.com/2021/01/commonsense-reasoning-for-natural.html){: target="_blank"} based on the [ACL 2020 Tutorial]() taught by [Maarten Sap](), [Vered Shwartz](), [Antoine Bosselut](), [Yejin Choi](), [Dan Roth]().**
</td>
</table>





### Our working definition

<table>
<td markdown="block" class="fs-4">

Commonsense reasoning is a human-like **ability** to make presumptions about ordinary **objects**, **events**, and **situations** that humans encounter every day. 
It can be seen a process of using commonsense knowledge to solve real-world problems, which we want to teach machines to do at the basic level.
Thus, it is one of the fundamental areas of Artificial Intelligence (AI) research.

Commonsense knowledge are facts that most people can acquire in their life by observing and interacting with the physical world and other humans.
Thus, there are two major topics in commonsense knowledge: physical and social common sense. 
Within each topic, the knowledge can be further characterized by their basic units and focused dimensions.


- **Physical** Commonsense Knowledge
    - `objects`{: .csk-label} (including both physical objects and abstract concepts)
        - `taxonomic`{: .csk-label} (e.g., *cat is an instance of animal*)
        - `properties`{: .csk-label} (e.g., *ice is cold*)
        - `part-whole`{: .csk-label} (e.g., *birds have two legs*)
        - `utility`{: .csk-label} (e.g., *oven is used for heating something up*)
        - `spatial`{: .csk-label} (e.g., *tables and chairs located near each other*)
        - `affordance`{: .csk-label} (e.g., *open a door; put an apple in a basket*)
        - etc.
    - `events`
        - `causality`{: .csk-label} (e.g., *using fossil fuel causes global warming*)
        - `spatial`{: .csk-label} (e.g., *cooking a meal happens in a kitchen*)
        - `duration`{: .csk-label} (e.g., *human's sleeping is about eight hours*)
        - `order`{: .csk-label} (e.g., *buying a ticket happens before taking on the airplane*)
        - `part-whole`{: .csk-label} (e.g., *preparing materials is part of cooking a meal*)
        - `time`{: .csk-label} (e.g., *people usually start working at 9 AM*)
        - `frequency`{: .csk-label} (e.g., *the presidential election happens every four year in US*)
        - etc.
- **Social** Commonsense Knowledge
    - `objects`{: .csk-label} (usually abstract concepts and human activities)
        - concepts (e.g., *friends help each other*)
        - activities (e.g., *marriage needs happiness*)
        - etc.
    - `events`{: .csk-label} (situations in everyday life)
        - `acceptability`{: .csk-label} (e.g., *commenting the weight/face/age of a co-worker is not accepted*)
        - `motivation`{: .csk-label} (e.g., *X buys Y a gift **because** X wanted to make Y happy, ...*)
        - `attributes`{: .csk-label} (e.g., *X buys Y a gift; X is seen as generous, polite, ...*)
        - `effect`{: .csk-label} (e.g., *X buys Y a gift; Y is surprised*)
        - etc.

<!-- - prerequisite - next-event (e.g., *having a cup of coffee usually happens after waking up*) -->

There are also other dimensions to describe a commonsense fact as follows: 
- `concreteness`{: .csk-label} (e.g., *birds have legs* < *birds have two legs*)
- `plausibility/typicality`{: .csk-label} (e.g., **most** birds have two legs > **some** apples are green)
- `saliency`{: .csk-label} (e.g., *birds have **wings*** > *birds have **legs*** )
- `cultural`{: .csk-label} (e.g., *high schools are four years in the **USA***, while *three years in **China***.)

<!-- Commonsense knowledge are rarely stated, and we usually take them for granted. -->

{: style="text-align:right; margin-bottom:0.1em" }
--- **[Bill Yuchen Lin]().**
</td>
</table>



## Why do we study commonsense reasoning?


<!-- Commonsense is essential for humans to navigate everyday situations seamlessly and interact with each other in a reasonable and safe way, and for AI to understand human needs and actions better. Yet, endowing machines with such human-like commonsense reasoning capabilities has remained an elusive goal of AI research for decades. Past attempts, in the 1960s and 1970s, resulted in an AI winter, i.e. reduced interest and funding for AI research due to failed over-hyped research directions. In recent years, new interest in machine commonsense has emerged, with the availability of stronger computing power and huge amounts of data. With that said, the path to machine commonsense is unlikely to be brute force training larger neural networks with deeper layers.    -->

 