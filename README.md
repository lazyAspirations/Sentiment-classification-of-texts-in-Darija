Sentiment Classification of Texts in Darija 🇩🇿🇲🇦
📌 Project Overview
This project focuses on the Sentiment Analysis of comments written in Darija (Maghrebi Arabic dialect). The system classifies texts into three categories: Positive, Neutral, and Negative. It leverages Natural Language Processing (NLP) techniques and the K-Nearest Neighbors (KNN) algorithm to handle the unique linguistic challenges of the dialect.

![Snippet of the code](https://github.com/lazyAspirations/Sentiment-classification-of-texts-in-Darija/blob/main/Doc/gbfdbfb.PNG?raw=true)

Developed by: Aissat Mohamed Moncef

🚀 Workflow & Methodology
1. Data Preprocessing
Since Darija is a non-standardized dialect, rigorous cleaning was required:

Noise Removal: Stripping punctuation and special characters using re.sub.

Normalization: Converting text to lowercase for uniformity.

Stop Words Removal: Using a custom list of Maghrebi-specific stop words (e.g., "باش", "واش", "دروك") to filter out non-informative terms.

Stemming: Utilizing the ISRIStemmer to reduce Arabic words to their roots.

2. Feature Extraction
The text is transformed into numerical data using the TF-IDF (Term Frequency-Inverse Document Frequency) method.

Max Features: 5,000.

Purpose: This gives higher weight to words that are meaningful for sentiment while downplaying common words.

3. Model Training & Evaluation
Algorithm: K-Nearest Neighbors (KNN) with n_neighbors=5 and cosine similarity metric.

Data Split: 80% Training / 20% Testing.

Metrics: Accuracy, F1-Score, and Confusion Matrix.

📊 Performance Analysis
The model evaluates itself using:

Confusion Matrix: To visualize where the model confuses "neutral" with "negative" or "positive."

Classification Report: Providing Precision, Recall, and F1-score for each class.

🛠️ Tech Stack
Language: Python 3

Data Handling: Pandas

Machine Learning: Scikit-learn

NLP: NLTK (Natural Language Toolkit)

Visualization: Matplotlib

⚙️ How to Run Locally
1. Clone the repository:
git clone https://github.com/lazyAspirations/Sentiment-classification-of-texts-in-Darija.git
cd Sentiment-classification-of-texts-in-Darija
2. Install dependencies:
pip install pandas scikit-learn nltk matplotlib
Run the analysis:
Execute the script to clean the data and train the model:
3. Run the analysis:
python script_name.py

📂 Project Structure
sentiment_comments.csv: The raw dataset.
sentiment_comments_cleaned.csv: Dataset after cleaning and stemming.
sentiment_comments_sample_predictions.csv: Final output comparing actual vs. predicted labels.
