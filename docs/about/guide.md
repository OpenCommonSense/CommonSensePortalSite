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

Commonsense reasoning is hard to define, although it has been . 
Basically, commonsense reasoning is the ability to make decisions in real-world situations with commonsense knowledge.
We show some existing definitions and characterizations (with modifications) . 


<table>
<td markdown="block" class="fs-4">
In artificial intelligence (AI), **commonsense reasoning is a human-like ability to make presumptions about the type and essence of ordinary situations humans encounter every day**. 
These assumptions include judgments about the nature of physical objects, taxonomic properties, and peoples' intentions. 
A device that exhibits commonsense reasoning might be capable of drawing conclusions that are similar to humans' **folk psychology** (i.e., *humans' innate ability to reason about people's behavior and intentions*) and **naive physics** (i.e., *humans' natural understanding of the physical world*). Some definitions and characterizations of common sense from different authors include:

1. "Commonsense knowledge includes the basic facts about events (including actions) and their effects, facts about knowledge and how it is obtained, facts about beliefs and desires. It also includes the basic facts about material objects and their properties." ([McCarthy, John; 1989]())
1. "Commonsense knowledge **differs from *encyclopedic* knowledge** in that it deals with *general* knowledge rather than the details of specific entities." ([Tandon et al. 2018](https://dl.acm.org/doi/10.1145/3186549.3186562))
1. Commonsense knowledge is "real world knowledge that can **provide a *basis*** for additional knowledge to be gathered and interpreted automatically". ([Matuszek, Cynthia, et al. 2005]())
1. The commonsense world consists of "**time, space, physical interactions, people,** and so on". ([Ernest Davis; Gary Marcus 2015](https://www.aaai.org/Library/AAAI/2005/aaai05-227.php))
1. Common sense is "all the knowledge about the world that we **take for *granted* but *rarely state*** out loud". ([Clive Thompson 2020](https://www.wired.com/story/how-to-teach-artificial-intelligence-common-sense/))
<!-- 1. Common sense is "broadly reusable background knowledge that's not specific to a particular subject area... knowledge that you ought to have." ([Pavlus, John; 2020](https://www.quantamagazine.org/common-sense-comes-to-computers-20200430/)) -->
<!-- 1. Commonsense knowledge is "what a typical seven year old knows about the world", including physical objects, substances, plants, animals, and human society". ([Davis, Ernest 2017](https://doi.org/10.1613%2Fjair.5339)) -->

</td>
</table>

{: style="text-align:right; margin-top:-1em"}
-- **(Modified) Wikipedia: [Commonsense Reasoning](https://en.wikipedia.org/wiki/Commonsense_reasoning){: target="_blank"}**

<table>
<td markdown="block" class="fs-4">

Common sense is the basic level of practical knowledge and reasoning concerning **everyday objects, situations, and events** that are commonly shared among most people. Commonsense knowledge can be categorized according to types, including but not limited to:


- **Physical common sense:** Physical common sense includes knowledge about the physical **properties** and **affordances** of everyday objects. 
<!-- For example, a glass will likely shatter if it falls to the floor, is a fact most people know.  -->


- **Social common sense:** People are capable of making inferences about other people's **mental states**, e.g. what *motivates* them, what they are *likely to do next*, etc. In addition, we each have a set of **social norms** of accepted behavior. These are often *implicit* in our actions and decisions. 

- **Temporal common sense:** natural language rarely communicates explicit temporal information. Instead it's vague and relies on the commonsense knowledge of the listener. 
<!-- For example, when told that "Dr. Porter is taking a vacation" we can predict that Dr. Porter will not be able to see us soon, as opposed to when "Dr. Porter is taking a walk".  -->
This requires knowing the **typical duration**, **times, order, frequency, etc. of events**.
<!-- "taking a walk" (minutes) and that of "taking a vacation" (days). Other temporal knowledge is  -->
 

</td>
</table>

{: style="text-align:right; margin-top:-1em"}
-- **(Modified) A [blog post](http://veredshwartz.blogspot.com/2021/01/commonsense-reasoning-for-natural.html){: target="_blank"} based on the [ACL 2020 Tutorial]() taught by [Maarten Sap](), [Vered Shwartz](), [Antoine Bosselut](), [Yejin Choi](), [Dan Roth]().**



## Why do we study commonsense reasoning?


<!-- Commonsense is essential for humans to navigate everyday situations seamlessly and interact with each other in a reasonable and safe way, and for AI to understand human needs and actions better. Yet, endowing machines with such human-like commonsense reasoning capabilities has remained an elusive goal of AI research for decades. Past attempts, in the 1960s and 1970s, resulted in an AI winter, i.e. reduced interest and funding for AI research due to failed over-hyped research directions. In recent years, new interest in machine commonsense has emerged, with the availability of stronger computing power and huge amounts of data. With that said, the path to machine commonsense is unlikely to be brute force training larger neural networks with deeper layers.    -->

 