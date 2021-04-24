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

Commonsense reasoning is hard to define. There are a list of quotes (with some modifications) about the definition of commonsense knowledge and reasoning. The content below mainly serve as a quick preview of the definitions from different people.


<table>
<td markdown="block" class="fs-4">
In artificial intelligence (AI), commonsense reasoning is a human-like ability to make presumptions about the type and essence of ordinary situations humans encounter every day. These assumptions include judgments about the nature of physical objects, taxonomic properties, and peoples' intentions. A device that exhibits commonsense reasoning might be capable of drawing conclusions that are similar to humans' folk psychology (humans' innate ability to reason about people's behavior and intentions) and naive physics (humans' natural understanding of the physical world).

Some definitions and characterizations of common sense from different authors include:

1. "Commonsense knowledge includes the basic facts about events (including actions) and their effects, facts about knowledge and how it is obtained, facts about beliefs and desires. It also includes the basic facts about material objects and their properties." ([McCarthy, John; 1989]())
2. "Commonsense knowledge differs from encyclopedic knowledge in that it deals with general knowledge rather than the details of specific entities." ([Tandon et al. 2018](https://dl.acm.org/doi/10.1145/3186549.3186562))
3. Commonsense knowledge is "real world knowledge that can provide a basis for additional knowledge to be gathered and interpreted automatically". ([Matuszek, Cynthia, et al. 2005]())
4. The commonsense world consists of "time, space, physical interactions, people, and so on". ([Ernest Davis; Gary Marcus 2015](https://www.aaai.org/Library/AAAI/2005/aaai05-227.php))
5. Common sense is "all the knowledge about the world that we take for granted but rarely state out loud". ([Clive Thompson 2020](https://www.wired.com/story/how-to-teach-artificial-intelligence-common-sense/))
6. Common sense is "broadly reusable background knowledge that's not specific to a particular subject area... knowledge that you ought to have." ([Pavlus, John; 2020](https://www.quantamagazine.org/common-sense-comes-to-computers-20200430/))
7. Commonsense knowledge is "what a typical seven year old knows about the world", including physical objects, substances, plants, animals, and human society". ([Davis, Ernest 2017](https://doi.org/10.1613%2Fjair.5339))

</td>
</table>

{: style="text-align:right; margin-top:-1em"}
-- **Modified from Wikipedia: [Commonsense Reasoning](https://en.wikipedia.org/wiki/Commonsense_reasoning){: target="_blank"}**

<table>
<td markdown="block" class="fs-4">

Commonsense is the basic level of **practical knowledge** and reasoning concerning everyday situations and events that are commonly shared among most people. The boundaries of commonsense are quite challenging to define, but we will go with this working definition: 
Commonsense is the basic level of practical knowledge and reasoning concerning everyday situations and events that are commonly shared among most people. 
For example, it's commonsense that it's OK to keep the closet door open, but not the fridge door, as the food inside might go bad. 

Commonsense knowledge can be categorized according to types, including but not limited to:

- **Social commonsense:** people are capable of making inferences about other people's mental states, e.g. what motivates them, what they are likely to do next, etc. This kind of inferences is captured by the ATOMIC knowledge base, discussed later. In addition, we each have a set of social norms of accepted behavior, e.g. knowing that “it's impolite to comment on someone's weight”. While these are often implicit in our actions and decisions, machines need to be taught them explicitly. 

- **Temporal commonsense:** natural language rarely communicates explicit temporal information. Instead it's vague and relies on the commonsense knowledge of the listener. For example, when told that "Dr. Porter is taking a vacation" we can predict that Dr. Porter will not be able to see us soon, as opposed to when "Dr. Porter is taking a walk". This requires knowing the typical duration of "taking a walk" (minutes) and that of "taking a vacation" (days). Other temporal knowledge is typical times, order, frequency, etc. of events which are addressed by the MC-TACO dataset and the TACO-LM time-aware contextual language model. 

- **Physical commonsense:** a glass will likely shatter if it falls to the floor, is a fact most people (and arguably cats) know. Physical commonsense includes knowledge about the physical properties and affordances of everyday objects, as tested in the PIQA dataset.

Commonsense is essential for humans to navigate everyday situations seamlessly and interact with each other in a reasonable and safe way, and for AI to understand human needs and actions better. Yet, endowing machines with such human-like commonsense reasoning capabilities has remained an elusive goal of AI research for decades. Past attempts, in the 1960s and 1970s, resulted in an AI winter, i.e. reduced interest and funding for AI research due to failed over-hyped research directions. In recent years, new interest in machine commonsense has emerged, with the availability of stronger computing power and huge amounts of data. With that said, the path to machine commonsense is unlikely to be brute force training larger neural networks with deeper layers.   

</td>
</table>

{: style="text-align:right; margin-top:-1em"}
-- **The [blog post](http://veredshwartz.blogspot.com/2021/01/commonsense-reasoning-for-natural.html){: target="_blank"} by [Vered Shwartz](https://vered1986.github.io/){: target="_blank"} about the ACL 2020 Tutorial.**


 