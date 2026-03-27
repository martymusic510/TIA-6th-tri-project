# TIA-6th-tri-project
MOOC project
# Banking App Review Sentiment and Topic Analysis

## 👥 Contributors
* Anirudh Gupta (055003)
* Devansh Pratap Singh (055037)
* Amartya Raj Singh (055053)
* Harsh Jain (055018)

## 📝 Project Details
This project involves performing a detailed sentiment and topic analysis on banking application reviews for HDFC Bank and Yono SBI. The primary goal is to understand user perceptions, identify key areas of satisfaction and dissatisfaction, and categorize common pain points using advanced Natural Language Processing (NLP) techniques.

## 🎯 Problem Statements
1. To understand the overall sentiment (positive, negative, neutral) of user reviews for HDFC Bank and Yono SBI mobile applications.
2. To identify and compare the effectiveness of traditional (VADER) versus advanced (RoBERTa) sentiment analysis models in classifying banking app reviews.
3. To pinpoint specific themes and recurring issues in both positive and negative reviews for each bank.
4. To uncover latent groupings of negative feedback (pain points) across both banking apps through clustering, enabling a deeper understanding of user grievances.

## 🛠️ Technologies Used
* *Python:* Programming language for analysis.
* *pandas & numpy:* For data manipulation, numerical operations, and analysis.
* *matplotlib & seaborn:* For data visualization.
* *nltk:* For natural language processing tasks such as tokenization, stopwords, and VADER sentiment scoring.
* *transformers (Hugging Face):* For implementing the pre-trained RoBERTa sentiment analysis model.
* *scikit-learn:* For TF-IDF vectorization, Truncated SVD, and K-Means clustering.

## 📊 Nature and Source of Data
The data consists of user reviews for the HDFC Bank and Yono SBI applications, sourced from CSV files (HDFC_Bank_Reviews.csv and Yono_SBI_Reviews.csv). Each dataset was downsampled to the first 500 rows for efficient processing during this analysis.

## ⚙️ Methodology & Key Activities
1. *Data Loading and Preprocessing:* Loading and initial cleaning of the review data.
2. *Sentiment Analysis:* Applying both VADER and RoBERTa models to classify reviews into Positive, Negative, and Neutral sentiments, followed by generating a comparative distribution table.
3. *Topic Extraction:* Identifying the top 10 most frequently discussed topics within positive and negative review subsets for each bank (after refining stopwords).
4. *Negative Review Clustering:* Combining all negative reviews from both banks and performing TF-IDF vectorization followed by Truncated SVD for dimensionality reduction.
5. *K-Means Clustering:* Employing the Elbow Method to determine the optimal number of clusters, applying K-Means clustering, and extracting top topics to identify distinct categories of user pain points.

## 📈 Key Observations

### 1. Sentiment Analysis Overview
| Bank | Method | Positive | Negative | Neutral |
| :--- | :--- | :--- | :--- | :--- |
| *HDFC* | VADER | 350 | 88 | 62 |
| *HDFC* | RoBERTa | 269 | 133 | 98 |
| *Yono SBI* | VADER | 255 | 149 | 96 |
| *Yono SBI* | RoBERTa | 178 | 216 | 106 |

* *Model Differences:* VADER identified a significantly higher number of positive reviews, while RoBERTa provided a stricter and arguably more accurate negative sentiment detection, categorizing more reviews as Negative or Neutral.

### 2. Pain Point Clusters (Combined Negative Sentiments)
Out of 349 total negative reviews clustered, the top issues identified were:
* *Core App Functionality & Login Issues (225 reviews):* The most prevalent pain point focusing on updates, login difficulties, and accessing accounts.
* *Version Change & Usability Problems (34 reviews):* Struggles with interface changes and usability due to new app versions.
* *App Not Working Properly (25 reviews):* Performance issues where the app fails to function correctly.
* *Recurring Experience & Login Issues (21 reviews):* Persistent negative experiences spanning several months.

## 💡 Overall Insights & Strategic Recommendations
From a market-level perspective, this analysis highlights key gaps in the existing banking app ecosystem:
* *Major Failure Points:* Authentication, core functionality stability, and account access are critical struggle areas for competitors.
* *Update Fatigue:* Frequent updates are perceived as harming the user experience by introducing bugs rather than improving the product.

*Recommendations for Market Entrants:*
* *Reliability:* Ensure zero-failure login systems and crash-free performance to build trust.
* *Stability Over Features:* Release well-tested, incremental updates instead of frequent disruptive changes.
* *Superior UX:* Design simple interfaces accessible to non-tech-savvy users.
* *Execution Excellence:* The biggest opportunity lies in delivering a stable, reliable product where competitors are currently failing.

## 🚀 How to Run
1. Clone this repository to your local machine.
2. Ensure you have Jupyter Notebook or JupyterLab installed.
3. Install the required dependencies:
   bash
   pip install pandas numpy matplotlib seaborn nltk transformers scikit-learn
   
4. Place the datasets (HDFC_Bank_Reviews.csv and Yono_SBI_Reviews.csv) in the appropriate /content/ directory or update the file paths in the notebook.
5. Open agdpsarshj03375318_sentiment_analysis_HDFC_SBI.ipynb and run the cells sequentially.
