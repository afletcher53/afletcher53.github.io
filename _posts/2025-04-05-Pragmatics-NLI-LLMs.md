---
layout: distill
title: Pragmatics & NLI within LLMs
date: 2024-04-03 00:00:00
description: A paper on how LLMs handle different pragmatic sentence types
tags: Journal Paper Pragmatics LLMs NLI
categories: ["Paper Review"]

authors:
  - name: Aaron Fletcher
    affiliations:
      name: Sheffield University
---

Today I wanted to share some thoughts on this paper, which I am reading as part of a small review on pragmatics within LLMs for a project that I am working on for over the next few months. 

The paper - When Truth Matters - Addressing Pragmatic Categories in Natural Language Inference (NLI) by large language models (LLMs) is a short article that attempts to do 4 things - Firstly detailing the notion of inference, secondly assess the extent of the phenomenon of non-assertive premises on a dataset, thirdly show how to 'acquaint' LLMs with these pragmatic categories and finally create a dataset for future researchers. 

I want to start out with that I am ***not*** a pragmatist by trade, and often a lot of these concepts are new to me (outside of knowing speech acts)! I do find the text surrounding pragmatics to be rather terminological dense, and that forms why I chose this paper to read - introduce me to some of the terminology used and also look at how people are applying these to large langauge models. 

**Introduction**

The introduction section serves it purpose well, delivering key definitions that are used throughout the paper: 
Entailment - where comitting to a truth of one statement commits you to the truth of others 

Inference, which can be divided into two forms, deductively valid references (where it is not logically possible that a premise is true while the conclusion is false), or inductively valid inferences, where is possible that the premise is true while the conclusion is false, but where the truth of the premise in general is a good reason for the truth of the conclusion. They further develop this by stating that for two utterences to entail (or contradict) each other they need to be of the correct pragmatic category.  The authors don't make clear what a pragmatic category is and I cant find much with my customary google search. 

They go on to state how questions and commands (unlike assertions or claims) do not abide by these rules as they do not involve making a claim that could be true or false, so they cannot contradict or entail each other. For example "Did Loral Harm National security" doesn't entail the speaker that national security is harmed. They use another example "Happy Hanukkah, everybody" which they claim does not bind the speaker to the state of affairs, however I am not quite convinced by this, as surely by saying this you are commiting yourself to the fact that it is Hanukkah (But again bear in mind I do not know enough about pragmatics to verify this).

I particularly enjoyed the justification given about why distinguishing between the types of pragmatic kinds of utterence is important, and it is something that will hopefully help me with my overall PhD topic: Fact checking needs to be able to distinguish between claims and statements vs questions as one does not commit the speaker to entailment. From my mind, this is potentially applicable in identifying when someone tries to state a fact, verses when they are searching for information. Additionally the justification of LLMs needing reasoning capabilities to distinguish between fact and fiction to prevent misinformation propegation was an important one. 

The authors go on to frame the way in which LLMs are taught in NLI, using two sentences one is the premise (P), the other is the hypothesis (H) and the LLM then predicts contradiction of these two sentences (contradiction, P and H cannot both be true, entailment: P being correct means H is correct, or neither).  They go on to outline the MLNI dataset:


(P) yes now you know if if everybody like in August when everybody's on vacation or something we can dress a little more casual or
(H) August is a black out month for vacations in the company.
 = Contradiction

(P) At the other end of Pennsylvania Avenue, people began to line up for a White House tour.
(H) People formed a line at the end of Pennsylvania Avenue.
= entailment


They point out that two large datasets dominate the field MNLI, and also SNLI (an image pair caption dataset) and their respective bias. The MNLI dataset, for example, when having a negation in the hypothesis is more likely to be a contradiction, however they do not state the magnitude of this bias (while the referencing paper does, I would have liked this spelt out!). They outline how they adapt work by Williamson. 

We finally get to the "meat" of the paper (at page 6!) where they outline their main experiment. They hypothesis that :
- models fine tuned on MNLI are insensitive to non assertive premises cannot entail or be contradicted by other premise
- This "deficit" can be amended using properly composed fine-tuning dataset
- This does not significantly harm performance on the original MNLI dataset. 

3 transformer based models were used that had been fine tuned on MNLI (DeBERTa-base, XLNET-base, and RoBERTa-Large). For me, very little justification was given as to why these three models were chosen besides "they have different architectures". Which, yes, they do, but I would have liked some discussion as to why the author's felt the difference might have resulted in differences in the output. 

Its getting a little long for me, so I will continue in a second part!

To be continued...





