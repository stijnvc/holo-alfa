---
layout: post
title: How to Choose the Right Metrics for Classification Models
categories: [blog, data-science]
tags: [data-science, machine-learning, metrics]
---

### Introduction
Classification models are widely used in data science and machine learning to predict a class for a given input. For example, given a picture of a dog, we need to predict if it’s a dog or not. However, how do we know if our model is accurate and reliable? How do we measure the performance of our model and compare it with other models? In this blog post, I will explain some common metrics for classification models, such as accuracy, precision, recall, and F1 score. I will also show you some examples and pitfalls of using these metrics, and how to choose the best metric for your problem and data.

The common sense tell us that the accuracy of our model can be measured simply by an accuracy metric, 
which divide the total correct predictions by the total number of observations.

The common sense is wrong.

For example, let's say we have a dataset of 1000 pictures of dogs and one picture of cat.
The model that always predict dog will have 99.9% accuracy, however, it's a bad model, 
for a different dataset (for example 1000 cats and one dog) it will have close to 0% accuracy.

Let's see some other metrics that can help us to evaluate model accuracy, the measerments are on the accuracy of specific class.

### Precision
- The number of **correct** predictions of a specific class divided by the total number of predictions of a **specific** class. 
  A hack to remember the meaning is by the Prec**is**ion word (is => this side of the model).

  For example:
  - We have a dataset of 1000 pictures of dogs and 1000 pictures of cats.
  - The model predict 500 of those pictures are dogs.
  - 400 of those pictures are actually dogs.
  - 100 of those pictures are actually cats.
  - The precision of the model is 400/500 = 80%.
  
### Recall
- The number of **correct** predictions of a specific class divided by the total number of observations. A hack to remember the meaning is by the Rec**all** word (all).
  For the example before, we can say:
    - The recall of the model is 400/1000 = 40%.


Since both precision and recall are important, we need a way to combine them into one metric, this metric is called F1 Score.

### F1 Score: 
- The harmonic mean of precision and recall. 
  
  The formula is: 
  ```math
  2 * (precision * recall) / (precision + recall)
  ```
  

  For the example before, we can say:
    - The F1 Score of the model is 2 * (0.8 * 0.4) / (0.8 + 0.4) = 0.53



