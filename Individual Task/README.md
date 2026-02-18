# My Personal Pattern Tracker: Track a week of your own choices (like songs listened to or products browsed) and analyze if a recommendation system could predict your next choice using supervised learning.

## 1. Introduction

Artificial Intelligence (AI) and Machine Learning (ML) are changing the way we interact with digital content. One common application is recommendation systems, which analyze user behavior to suggest personalized content such as songs, movies, or products.

In this task, I tracked my personal music listening habits for one week to study:

- How patterns in human behavior can be identified
- How supervised learning algorithms can predict future choices
- How AI can provide personalized recommendations

This hands-on approach bridges the gap between theory and real-life applications, showing how small datasets can still reveal meaningful patterns.

## 2. Objective

The main goals of this individual task are:

- Collect personal behavioral data over a period of one week.
- Identify patterns in the data.
- Apply supervised learning techniques to predict future behavior.
- Analyze the reliability of predictions.
- Understand the foundation of AI-powered recommendation systems.

## 3. Understanding the Machine Learning Concept

This task falls under **Supervised Learning**, because:

- The data is labeled: the “Genre” is the known output.
- The input features (Time, Mood, Language) are given.
- The goal is to classify new instances based on these features.

It is a **classification problem** because the output is categorical (Genre: Devotional, Pop, or Melody).

**Supervised learning works by:**

- Learning the relationship between inputs (features) and outputs (labels)
- Building a predictive model
- Testing the model’s accuracy on new unseen data

This is exactly how modern AI systems recommend songs or movies based on user behavior.

## 4. Data Collection

Data was collected manually over 7 days. Each day, I noted:

- **Time of listening:** Morning, Evening, Night  
- **Mood during listening:** Calm, Energetic, Relaxed, Sad  
- **Language preference:** Tamil, Hindi, English  
- **Genre chosen:** Devotional, Pop, Melody  

The collected dataset is small but sufficient to demonstrate pattern recognition.

## 5. Sample Dataset
![WhatsApp Image 2026-02-18 at 2 33 36 PM](https://github.com/user-attachments/assets/0381551b-3aa7-4299-a879-548396ab7795)

## 6. Feature and Target Variable

**Input Features (Independent Variables):**

- Time
- Mood
- Language

**Target Variable (Dependent Variable):**

- Genre (Devotional, Pop, Melody)

The model uses input features to predict the output genre.

## 7. Data Preprocessing

Before training, the data must be prepared. Machine learning models process numerical values, so categorical features must be converted.

**Encoding:**

- Time: Morning=0, Evening=1, Night=2  
- Mood: Calm=0, Energetic=1, Relaxed=2, Sad=3  
- Language: Tamil=0, Hindi=1, English=2  
- Genre (Target): Devotional=0, Pop=1, Melody=2  

**Benefits of Preprocessing:**

- Makes data usable by algorithms  
- Ensures consistent representation  
- Reduces errors in learning  

Preprocessing also includes checking for missing or inconsistent data, but in this controlled dataset, no missing data exists.

## 8. Exploratory Data Analysis (EDA)

Before modeling, the data can be analyzed for patterns:

**Observed Patterns:**

- Morning + Calm + Tamil → Devotional (Repeated on Mon & Thu)  
- Evening + Energetic + English → Pop (Repeated on Tue, Fri, Sun)  
- Night + Sad/Relaxed + Hindi → Melody (Wed & Sat)  

**Insights:**

- Mood strongly influences genre selection.  
- Time of day correlates with genre (Morning → Devotional, Evening → Pop).  
- Language preference is a consistent indicator.  

This shows the data contains predictable patterns, suitable for supervised learning.

## 9. Model Selection

Given the dataset and task type, suitable algorithms include:

- **Decision Tree**  
  - Handles categorical features well  
  - Creates clear decision rules  
  - Easy to visualize

- **K-Nearest Neighbors (KNN)**  
  - Predicts output based on nearest similar instances  
  - Sensitive to feature representation

- **Logistic Regression (Multinomial)**  
  - Can handle multi-class classification  
  - Provides probability estimates

- **Naïve Bayes**  
  - Based on probability  
  - Works well for small datasets

For this task, **Decision Tree** is ideal due to simplicity, interpretability, and handling of small datasets.

## 10. Training Process

**Steps:**

1. Split the dataset into:  
   - Training set (e.g., 5–6 days)  
   - Testing set (remaining days)

2. Train the algorithm:  
   - Learn patterns in input features  
   - Map (Time, Mood, Language) → Genre

3. Check for overfitting:  
   - Small dataset may cause memorization  
   - Cross-validation can help if dataset is larger

4. Testing:  
   - Use testing data to see if model predicts correctly

5. Error Analysis:  
   - Compare predicted genre with actual genre  
   - Correct errors by understanding feature influence

## 11. Prediction Examples

- **Input:** Time=Evening, Mood=Energetic, Language=English → **Prediction:** Pop  
- **Input:** Time=Morning, Mood=Calm, Language=Tamil → **Prediction:** Devotional  
- **Input:** Time=Night, Mood=Relaxed, Language=Hindi → **Prediction:** Melody  

This demonstrates that the model captures human listening patterns effectively.

## 12. Model Evaluation Metrics

For small datasets:

- **Accuracy** = Number of correct predictions / Total predictions  
- **Precision** = Correct positive predictions / Total predicted positives  
- **Recall** = Correct positive predictions / Total actual positives  
- **F1 Score** = Harmonic mean of Precision and Recall

**Example (based on dataset):**

- Total predictions = 7  
- Correct predictions = 7  
- Accuracy = 100% (for small sample, though may not generalize)

## 13. Limitations

- Dataset is small (7 records) → limited generalization  
- Human behavior can vary day-to-day  
- Mood and other features can be subjective  
- External factors (friends, events, weather) not included  
- Model may overfit due to repetitive patterns  

**Solution:** Collect data for 1–2 months to improve prediction reliability.

## 14. Real-World Application

Recommendation systems like Spotify, YouTube, Amazon, Netflix work similarly:

- Collect behavioral data automatically  
- Track time, preferences, and patterns  
- Use supervised or deep learning algorithms  
- Predict next choice for personalized experience  

Our task is a simplified version of these systems.

## 15. Feature Importance Analysis (Conceptual)

In a Decision Tree:

- **Time** splits the first level  
- **Mood** splits second level  
- **Language** splits third level  

**Example:**  
- Morning + Calm → Devotional → 100% prediction  
- Evening + Energetic + English → Pop → 100% prediction  

Feature analysis helps in understanding personal behavior.

## 16. Improvement Strategies

To enhance prediction accuracy:

- Track data over a longer period (30–60 days)  
- Include more features:  
  - Weather (Sunny / Rainy)  
  - Day type (Weekday / Weekend)  
  - Device used (Phone / Laptop)  
  - Frequency and rating of songs  
- Use more advanced models if dataset grows (Random Forest, Gradient Boosting)

## 17. Conclusion

- Personal behavior exhibits patterns that AI can learn.  
- Supervised learning can predict next music choice based on prior patterns.  
- Small datasets work for demonstration; larger datasets improve reliability.  
- Recommendation systems operate on similar principles.  
- Features such as Time, Mood, and Language are critical for accurate predictions.  

This task demonstrates a practical application of ML in everyday life and strengthens understanding of supervised learning concepts, feature selection, model training, evaluation, and prediction.

