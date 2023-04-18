----

## Overview
- ML basics
- Neural Networks
- Backpropagation
- Optimization
- CNNs
- RNNs
- Transformers etc

## Context

- **Artificial Intelligence**: very broad field, anything that mimics intelligence
	- e.g. if statements, search algorithms, logic, etc
- **Machine Learning**: subset of AI, characterized by learning
	- e.g. Linear/Logistic Regression, SVM, Random Forests
- **Learning**: here means learning from data, aka training data -> behavior

>**DEEP LEARNING**: specifically learning methods that utilize neural networks
>e.g. Multi-layer perceptrons, CNNs, RNNs, Transformers, Generative models
  → this lecture: math behind that + applications!
 
#### Applications of Deep Learning (or learning in general):
- computer vision: historically first field, hence will guide us through the lecture
- medical imaging
- robotics: ties in with computer vision
- NLP: translations, LLM (large language models)
- computer graphics: image as an output

#### The case of Computer Vision

##### The beginnings
- 60s: mimic human visual system -> center block of robotic intelligence
- Hubel and Wiesel: neurobiologists; experimented to find out how human vision system works
- experiment setup: visual patterns vs patterns in brain activity → result: visual cortex cells sensitive to orientation of edges but insensitive to position

>Concept applies eg in CNNs as well: be invariant to certain features while focusing on others

- MIT summer vision project: visual pattern recognition

##### Today
- connected to many other fields: NLP, Neuroscience, Algorithms Optimization, many application fields
- fundamental motivation for evolution of Deep Learning

##### A computer vision problem: Image Classification
- label/categorize images
- pre-2012: feature extraction → learning algorithm → label assignment
	- ML but not DL
	- hand-crafted feature detectors
	- eg SIFT: scale-invariant feature transform → all invariant in some way
- 2012 breakthrough
	- magicbox of deep learning: unifies feature extraction and label assignment

> **end-to-end**: optimization regarding labels helps tune the whole process 


## Motivation

#### Deep Learning History
- 1940: electronic brain as a state machine made up of neurons + weights ([McCulloch-Pitts](https://de.wikipedia.org/wiki/McCulloch-Pitts-Zelle)) 
- 1957: [Perceptron](https://de.wikipedia.org/wiki/Perzeptron) - first model learning weights from training samples (Rosenblatt)
- 1960: [ADALINE](https://de.wikipedia.org/wiki/Adaline-Modell) - adaptive linear element (Widrow-Hoff)
- 1970: [XOR Problem](https://de.wikipedia.org/wiki/Perzeptron#XOR-Problem) - XORs cannot be represented linearly (Minsky-Papert)
	- thus begun the dark age of the AI Winter
- 1986: [Multi-Layered Perceptrons](https://de.wikipedia.org/wiki/Perzeptron#Mehrlagiges_Perzeptron) and [Backpropagation](https://de.wikipedia.org/wiki/Backpropagation) (Rumelhart, Hinton, Wiliams)
	- solves nonlinearly separable problems
	- theory for most modern DL technologies was already figured out in the 80s!
- 1995: SVMs - human intervention via kernel function (Vapnik, Cortes)
- 2006: Deep Neural Networks and Pre-training (Hinton, Ruslan)
- 2012: DL models start outperforming other models by a LOT 
	- [ImageNet](https://de.wikipedia.org/wiki/ImageNet) test (top-5 error)

#### What happened in 2012?
- more data available
	- e.g. MNIST digit recognition dataset (1998): 10^7 pixels vs ImageNet dataset: 10^14 pixels
- modern GPUs are good at (parallel) Matrix Vector Multiplications
- models have gotten more complex
- recognition: 2019 Turing award
- CVPR, ICCV: computer vision conferences - proportion + absolute number of papers using DL skyrocketed since then
- subtrends: GANs, LSTMs

#### Current topics of Computer Vision
- object detection/classification
- healthcare - very impactful currently
	- number of machines/scans grew much faster than number of professionals able to interpret the results
- entertainment
	- SOtA chess engines have only been using DL for 2 years
	- AI for starcraft?? → imitation + reinforcement learning
- emoticon suggestion
- machine translation
- google LaMDA: interactive language model
- Chat-GPT of course
- image generation/synthesis from text: DALL-E, Stable Diffusion
- video generation from text
- big market for DL technologies → good job opportunities :D


## Miscellaneous

#### Challenges of working with DL
- need in-depth knowledge
- very competitive

#### DL at TUM
- visual computing lab
- 3D Ai lab
- Computer Vision Group
- Data Mining and ANalytics Lab
- COmputer Aided Medical Procedures

multi-object tracking