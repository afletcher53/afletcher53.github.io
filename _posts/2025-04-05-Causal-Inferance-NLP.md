---
layout: distill
title: "Paper review: Causal Inference in Natural Language Processing:
Estimation, Prediction, Interpretation and Beyond"
date: 2024-04-03 00:00:00
description: A paper on how causality not correlation should be used to advance NLP
tags: Journal Paper Causality NLP LLMs
categories: ["Paper Review", "Journal Club"]

authors:
  - name: Aaron Fletcher
    affiliations:
      name: Sheffield University
---


**Introduction:**
As part of our NLP coursework, I read the paper ["Causal Inference in Natural Language Processing: Estimation, Prediction, Interpretation and Beyond"](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00511/113490/Causal-Inference-in-Natural-Language-Processing). This paper is highly relevant to my research interests in applying causal inference methods to text data. In this review, I will summarize the key ideas, discuss the strengths and weaknesses, and reflect on the implications for future work.

**Key Points:**
- The paper aims to clarify the differences between causal inference and prediction tasks in NLP
- It introduces key concepts such as counterfactuals, average treatment effect (ATE), conditional average treatment effect (CATE), and assumptions like ignorability, positivity, and consistency 
- The authors discuss the challenges of estimating causal effects with textual confounders and propose approaches like propensity score matching and data augmentation

**Strengths:**
- Provides a clear introduction to causal inference concepts and their relevance to NLP
- Offers a balanced discussion of the shortcomings of purely predictive models and the potential benefits of causal approaches
- Includes helpful mathematical formulations and illustrative examples throughout
- The section on data augmentation with counterfactuals was especially insightful and applicable to my work

**Weaknesses:**
- The introduction could better clarify the distinction between causal inference and prediction upfront
- Some examples, such as the gendered avatar experiment, felt outdated and insensitive
- The discussion of the training-test distributional shift was unclear and unsupported; this is a known issue in the field
- Overuses the "black box" characterization of deep learning models without nuance

**Suggestions for Improvement:**
- Provide a crisper definition of causal inference and prediction in the introduction and use more current examples 
- Avoid broad generalizations about deep learning models and acknowledge ongoing work on interpretability
- Expand the discussion of potential applications and provide more concrete guidance for practitioners

**Conclusion:**
Overall, this paper provides a valuable overview of causal inference methods for NLP and highlights essential challenges and future directions. Despite some areas for improvement in framing and examples, the authors make a compelling case for the benefits of causal approaches over purely predictive ones. The mathematical formulations and methodological suggestions will undoubtedly be helpful references for researchers working on related problems.

**Reflection:**
Reading this paper has made me think more deeply about the limitations of the predictive models I currently use in my research and the potential for causal inference techniques to address issues of robustness, fairness, and interpretability. I am particularly eager to explore the idea of counterfactual data augmentation to improve model performance and mitigate spurious correlations.