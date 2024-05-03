---
title: "Global explanations in LLMs"
date: 2024-05-03T20:33:03+08:00
draft: false
tags: ["deep-learning"]
description: A few techniques to generate global explanations for LLMs
---

Global explanations aim to offer insights into the inner workings of an LLM by understanding what individual components have encoded. Here, individual components could be neurons, hidden layers or even larger modules. In this post, we will look at four main methods -- probing, neuron activation analysis, concept-based methods and mechanistic interpretation.

## Probing-based methods

During self-supervised pre-training, LLMs acquire broad linguistic knowledge from training data. Using probing techniques, we can understand the knowledge that the LLMs have captured. There are two kinds of probing.

The first kind, called classifier-based probing, fits a shallow classifier on top of pre-trained or fine-tuned models.
- First, the parameters of the base model is frozen and the model generates representations for input words, phrases, or sentences.
- These representations are fed into the probe classifier, which is used to identify certain linguistic properties of reasoning abilities acquired by the model.
- After training, the probe is evaluated on a holdout dataset.

The second type of probing, are data-centric methods called parameter-free probing does not require probing classifiers.
- First, a dataset are designed tailored to a specific property you want to test.
- The base model's performance on this dataset give insights into it's capability in capturing this property.

Data-driven prompt search is another technique where certain knowledge is examined via language model's text generation or completion capabilities.

## Neuron Activation Explanation
This technique tries to find methods to understand the activation patterns in a model. To identify the roles of specific neurons in a specific neurons in a model, particularly in relation to learning and processing linguistic properties, this simple method can be used.
- First, important neurons can be identified in an unsupervised manner. This can be done by identifying neurons that are consistently active across many inputs.
- Relationship between these important neurons and particular linguistic properties can be identified using supervised tasks.
- Most important neurons can be found by comparing the correlation metrics between their activations and the linguistic properties, or the weights learned during supervised training.

## Concept-Based Explanation
Concept-based interpretability algorithms like Testing with Concept Activation Vectors (TCAVs) map the input data to a higher level, human-understandable concepts and explain the predictions of a model using the predefined concepts.
- First, we need to define a set of concepts that might be important for the model's decisions.
- For each concept, we need to then find a group of examples that represent them. These examples are then used to train concept activation vectors (CAVs). CAVs are direction vectors in a model's embedding space that point in the direction of a concept.
- TCAV then learns a linear classifier that acts as the CAV. This vector then serves as the boundary that differentiates between activations caused by the presence of a concept and those that are not related to it.
- Once the CAV is established, TCAV uses directional derivatives to measure how changes in the direction of the input space affects the model's predictions. This is done by perturbing the input along the direction of CAV and seeing how the output changes.
- The result of this is an importance score that defines quantifies the contribution of this concept to the model's predictions. A high TCAV score for a concept means that the model's predictions are sensitive to changes in the direction of this concept, indicating a high influence on predictions.

The difficulty in defining useful concepts and the need to collect examples for each concept is a challenge in using concept-based explanations.

## Mechanistic Interpretability
Mechanistic interpretability focusses on dissecting and understanding the complex network of neurons and their interconnections. This helps to understand how specific components of the model contribute causally to it's behaviour and outputs.

In this post, we looked at a few techniques for generating global explanations for LLMs.
These are my notes from the following paper:

> H. Zhao *et al.*, “Explainability for Large Language Models: A Survey,” *ACM Trans. Intell. Syst. Technol.*, vol. 15, no. 2, p. 20:1-20:38, Feb. 2024, doi: [10.1145/3639372](https://doi.org/10.1145/3639372).  

