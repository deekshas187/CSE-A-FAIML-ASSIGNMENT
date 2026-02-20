## 1. Variance and Bias (Diagram, overfit, underfit) - For best fit model should we have low bias or high variance, low bias or low variance, 
high bias or high variance, low bias or high variance

## 1.1 Introduction

In Machine Learning, when we build a model, our main goal is to make accurate predictions on new, unseen data. However, models often make two types of errors:

- Bias Error  
- Variance Error  

Understanding bias and variance helps us identify whether a model is overfitting or underfitting, and how to improve it.

---

## 1.2 What is Bias?

### Definition

Bias is the error caused by overly simple assumptions in the learning algorithm.

It measures how far the model’s predictions are from the actual values on average.

### Characteristics of High Bias

- Model is too simple  
- Cannot capture complex patterns  
- High training error  
- High testing error  
- Leads to Underfitting  

### Example

If we use a straight line (linear model) to fit curved data, the model cannot capture the curve properly. This is high bias.

---

## 1.3 What is Variance?

### Definition

Variance is the error caused due to too much sensitivity to small changes in training data.

It measures how much the model prediction changes when we use different training datasets.

### Characteristics of High Variance

- Model is too complex  
- Fits noise in data  
- Very low training error  
- High testing error  
- Leads to Overfitting  

### Example

If we use a very high-degree polynomial that passes through every data point, it fits training data perfectly but performs poorly on new data.

---

## 1.4 Bias–Variance Diagram (Conceptual Representation)

<img width="1536" height="1024" alt="ChatGPT Image Feb 20, 2026, 06_21_47 PM" src="https://github.com/user-attachments/assets/14182c65-665c-44cf-868a-865ca5134dc5" />

### Explanation

- Left side → Model too simple → High Bias → Underfitting  
- Right side → Model too complex → High Variance → Overfitting  
- Middle → Balanced model → Best performance  

---

## 1.5 Underfitting

### Definition

Underfitting occurs when the model is too simple to capture the pattern of the data.

### Causes

- Very simple model  
- Too few features  
- Less training time  

### Characteristics

- High Bias  
- Low Variance  
- Poor performance on both training and test data  

---

## 1.6 Overfitting

### Definition

Overfitting occurs when the model learns both pattern and noise in the training data.

### Causes

- Very complex model  
- Too many parameters  
- Small dataset  

### Characteristics

- Low Bias  
- High Variance  
- Excellent training accuracy  
- Poor test accuracy  

---

## 1.7 Bias–Variance Tradeoff

There is always a tradeoff between bias and variance:

- If bias decreases → variance increases  
- If variance decreases → bias increases  

The goal is to find a balance between them.

This balance is called the **Optimal Model** or **Best Fit Model**.

---

## 1.8 Optimal Model Selection

- Low Bias or High Variance → Overfitting  
- High Bias or High Variance → Worst case  
- High Bias or Low Variance → Underfitting  
- Low Bias and Low Variance → Correct Answer  

### Final Answer:

For the best fit model, we should have:

 **Low Bias and Low Variance**

Because:

- Low bias → Model captures true pattern  
- Low variance → Model generalizes well to new data  

---

## 1.9 Conclusion

Bias and variance are two main sources of error in machine learning models.

**Bias** occurs when a model is too simple and fails to capture the true pattern of the data, leading to **underfitting** and poor performance on both training and test data.

**Variance** occurs when a model is too complex and learns noise from the training data, leading to **overfitting** and poor performance on unseen data.

This relationship is called the **bias–variance tradeoff**:

- Increasing model complexity → Bias decreases, Variance increases  
- Decreasing model complexity → Bias increases, Variance decreases  

The best-fit model has **low bias and low variance**, meaning it captures real patterns while generalizing well to new data.

Techniques like cross-validation, regularization (L1/L2), increasing training data, and proper model selection help maintain this balance.

Balancing bias and variance is essential for building accurate and reliable machine learning models.
