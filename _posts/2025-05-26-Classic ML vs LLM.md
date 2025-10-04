---
layout: post
title: "Classic vs LLM"
subtitle: "Quick Decision Workflow"
background: '/img/posts/Automl/automl_background.jpg'
---
## Introduction
With the rapid advancement of large language models (LLMs), organizations increasingly face the question of when to leverage traditional machine learning (classic ML)versus LLMs for their use cases. This blog explores the key differences between these approaches, examines important considerations and trade-offs, and provides a practical decision framework to help you choose the right solution for your specific needs.

## What is classic ML or traditional Machine Learning?
Classic Machine Learning (ML) refers to models that learn from data to make predictions or decisions, often using structured or semi-structured data. Some key points are:
1. Can be categorized as supervised (classification & regression), unsupervised (clustering) or reinforcement learning.
2. Popular classic ML techniques include decision trees, random forests, support vector machines, logistic regression, and gradient boosting methods like XGBoost and LightGBM
3. Requires feature engineering; data scientists define features or transformations of raw data.
4. Typically works with structured data (numerical, categorical) though some ML methods also work with text/images when properly processed.

## What are Large Language Models (LLM)?
Large Language Models (LLMs) are advanced AI systems trained on vast amounts of text data to understand and generate human-like language.
1. Built on transformer neural networks with billions of parameters that capture complex language patterns and relationships
2. Uses unsupervised learning on massive text corpora, learning to predict the next word in sequences, which develops understanding of grammar, context, and knowledge
3. Capabilities can perform diverse tasks such as text generation, summarization, translation, question answering, code generation, and reasoning without task-specific training
4. Generative in nature and produces new content rather than just classifying or predicting from existing categories, enabling creative and contextual responses
representations from vast text data and can generalize to diverse tasks through natural language prompts.

## Cheat sheet to decide when to use LLM vs Classic ML?

**Decision Flow: Classic ML vs LLM**

Step 1: What kind of data do you have?
* Structured/tabular data (numbers, categories, metrics) :arrow_right: lean toward classic ML.
* Unstructured data (text, documents, conversations, multimodal content) :arrow_right: lean toward LLMs.
 
Step 2: What is the primary task?
* Prediction (classification, regression, forecasting, anomaly detection, churn modeling, risk scoring, etc.) :arrow_right: Classic ML is usually more efficient and interpretable.
* Understanding or generating natural language (summarization, Q&A, chatbot, content creation, semantic search, translation, document analysis) :arrow_right: : LLMs excel.
 
Step 3: What are your constraints?
* Need interpretability / explainability (finance, healthcare, regulated industries)? :arrow_right: Classic ML.
* Okay with some “black box” reasoning as long as accuracy and usability are high? :arrow_right: LLM.
* Limited compute resources, real-time latency requirements? :arrow_right: Classic ML is leaner.
* Ample compute budget, batch or asynchronous tasks? :arrow_right: LLM is fine.
 
Step 4: How much data do you have?
* Small labeled dataset, structured features :arrow_right: Classic ML (tree-based methods often excel).
* Large amounts of unstructured data (millions of documents, user queries, transcripts, reviews) :arrow_right: Pre-trained LLMs (possibly fine-tuned).
 
Step 5: Is hybrid best?

Often the best approach is to combine both:
* Use LLMs to preprocess or embed text into structured vectors, then feed into classic ML for prediction.
* Use classic ML models to score or validate outputs of LLMs.

![ClassicMLLLM](/img/posts/ClassicMLLLM/Picture1.png)


## Sources
1. <Jordan, M. I., & Mitchell, T. M. (2015). "Machine learning: Trends, perspectives, and prospects." Science, 349(6245), 255–260. https://doi.org/10.1126/science.aaa8415>
2. <Domingos, P. (2012). "A few useful things to know about machine learning." Communications of the ACM, 55(10), 78–87. https://doi.org/10.1145/2347736.2347755>
3. </Aswani, A., et al. (2017). "Attention Is All You Need." Advances in Neural Information Processing Systems (NeurIPS). https://arxiv.org/abs/1706.03762>
4. <Bommasani, R., et al. (2021). "On the Opportunities and Risks of Foundation Models." Stanford HAI. https://arxiv.org/abs/2108.07258>
5. <Zhang, C., & Bengio, Y. (2021). "Bridging machine learning and deep learning for tabular data." arXiv preprint. https://arxiv.org/abs/2106.03253>