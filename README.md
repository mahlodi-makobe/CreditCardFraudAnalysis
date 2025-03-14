# Credit Card Fraud Detection Using Unsupervised Learning

## Table of Contents
1. [Introduction](#introduction)
2. [Objective](#objective)
3. [Dataset](#dataset)
4. [Approach](#approach)
5. [Key Focus Areas](#key-focus-areas)
6. [Results](#results)
7. [Conclusion](#conclusion)
8. [How to Use This Repository](#how-to-use-this-repository)
9. [Dependencies](#dependencies)
10. [License](#license)

---

## Introduction
Fraud detection is a critical challenge for financial institutions, as fraudulent activities can lead to significant financial losses and damage to reputation. Traditional rule-based systems often struggle to detect new and evolving fraud patterns, making it essential to leverage advanced machine learning techniques for proactive fraud detection.

In this project, we worked with **Company ABC**, a major credit card company facing challenges with their existing fraud detection system. The current system exhibits slow responsiveness in recognizing new fraud patterns, leading to significant financial losses. To address this issue, we designed and implemented an **unsupervised learning-based fraud detection system** using transaction data provided by Company ABC.

---

## Objective
The primary goal of this project is to build an advanced fraud detection system that can efficiently identify and flag potentially fraudulent transactions for further investigation. By applying unsupervised learning algorithms, we aim to detect unusual transaction patterns that may indicate fraudulent activity.

---

## Dataset
The dataset consists of two tables:
1. **cc_info.csv**: Contains general credit card and cardholder information, including:
   - `credit_card`: Unique identifier for each credit card.
   - `city`, `state`, `zipcode`: Location of the cardholder.
   - `credit_card_limit`: Credit limit associated with the card.

2. **transactions.csv**: Contains details of credit card transactions that occurred between August 1st and October 30th, including:
   - `credit_card`: Unique identifier for each transaction.
   - `date`: Date and time of the transaction.
   - `transaction_dollar_amount`: Dollar amount of the transaction.
   - `Long`, `Lat`: Geographical coordinates of the transaction location.

---

## Approach
We used **unsupervised learning** techniques to detect anomalies in the transaction data. The key steps in our approach include:
1. **Data Preprocessing**: Merging datasets, handling missing values, and creating new features.
2. **Feature Engineering**: Extracting time-based features (e.g., day of the week, hour of the day) and calculating transaction patterns.
3. **Anomaly Detection**: Implementing three unsupervised learning algorithms:
   - **Isolation Forest**
   - **Local Outlier Factor (LOF)**
   - **One-Class SVM**
4. **Evaluation**: Analyzing the results and identifying common patterns among the flagged transactions.
5. **Visualization**: Creating visualizations to highlight anomalies and trends in the data.

---

## Key Focus Areas
- **Time Series Analysis**: Analyzing transaction patterns over time to identify unusual trends.
- **Unsupervised Anomaly Detection**: Using algorithms to detect transactions that deviate significantly from normal behavior.
- **Data Visualization**: Creating visualizations to communicate insights effectively.

---

## Results
1. **Anomalies Detected**:
   - **Isolation Forest**: Flagged **2,946 high-value transactions** with an average amount of **$929.19**.
   - **Local Outlier Factor (LOF)**: Flagged **2,946 smaller transactions** with an average amount of **$87.20**.
   - **One-Class SVM**: Flagged **2,949 transactions** with a mix of small and large amounts, averaging **$419.17**.

2. **Overlap Between Algorithms**:
   - **85 transactions** were flagged by all three algorithms.
   - These transactions are highly suspicious due to their high value and frequency.

3. **Common Characteristics of Anomalies**:
   - High transaction amounts (close to $1,000).
   - High transaction frequency (many transactions in a short time).
   - Unusual time intervals between transactions.

---

## Conclusion
By implementing unsupervised learning algorithms, we successfully identified potentially fraudulent transactions in Company ABC’s dataset. The combination of **Isolation Forest**, **Local Outlier Factor (LOF)**, and **One-Class SVM** provided a robust and scalable solution for fraud detection. The results demonstrate the effectiveness of unsupervised learning in detecting unusual transaction patterns, even in the absence of labeled data.

---

## How to Use This Repository
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/credit-card-fraud-detection.git
   cd credit-card-fraud-detection
