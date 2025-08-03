Netflix Clustering Analysis
This project explores unsupervised clustering techniques on the Netflix Movies and TV Shows dataset to identify distinct groups based on textual and categorical metadata. The goal is to segment content into meaningful clusters that reflect similarities in genre, cast, country, ratings, and description.

Project structure
Dataset
netfix_clustering.ipynb      # Main notebook performing clustering and visualization
README.md 

📌 Key Steps
1. Problem Statement

To group Netflix titles into clusters based on metadata and description content.

2. Know Your Data

Load and examine the dataset to understand columns like type, title, cast, director, description, listed_in, country, etc.

Understanding Your Variables

Feature selection and analysis of categorical/textual columns.

3. Exploratory Data Analysis (EDA)

Visualizations and statistics on content ratings, genres, and country-wise distribution.

4. Data Cleaning

Handling missing values, formatting inconsistencies, and duplicates.

5. Textual Data Preprocessing

NLP preprocessing: tokenization, stopword removal, lemmatization of the description column.

6.  Implementation

Dimensionality reduction using TF-IDF + Truncated SVD

Clustering using KMeans, cluster visualization with word clouds and PCA.

7. Recommendation System (Optional)

Based on cluster similarity (if implemented).

8. Conclusion

Interpretation of clusters and key takeaways.


🛠️ Technologies Used
Python

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

NLTK, WordCloud

Jupyter Notebook



