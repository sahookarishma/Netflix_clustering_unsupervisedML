# Netflix Movies and TV Shows Clustering - Unsupervised Machine Learning

## Project Overview

This project implements unsupervised machine learning techniques to cluster Netflix movies and TV shows based on their content characteristics. The goal is to discover natural groupings in the Netflix catalog and build a content-based recommendation system.

## Objectives

- **Content Clustering**: Group similar Netflix titles using unsupervised learning algorithms
- **Pattern Discovery**: Identify natural clusters in the Netflix catalog
- **Recommendation System**: Build a content-based recommendation engine
- **Data Analysis**: Perform comprehensive exploratory data analysis on Netflix content

## Dataset

**NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv**
- **Size**: 2.9MB
- **Content**: Netflix movies and TV shows catalog
- **Features**: 12 columns including title, type, director, cast, country, release_year, rating, duration, listed_in, description

### Key Features:
- `show_id`: Unique identifier for each title
- `type`: Movie or TV Show
- `title`: Name of the content
- `director`: Director(s) of the content
- `cast`: Main cast members
- `country`: Country of origin
- `date_added`: When content was added to Netflix
- `release_year`: Year of original release
- `rating`: Content rating (TV-MA, TV-14, etc.)
- `duration`: Length of content
- `listed_in`: Genre categories
- `description`: Content description

## Methodology

### 1. Data Preprocessing
- **Text Cleaning**: Removed non-ASCII characters, stopwords, and punctuation
- **Feature Engineering**: Combined director, cast, country, and description into clustering attributes
- **Text Normalization**: Converted to lowercase and applied stemming
- **TF-IDF Vectorization**: Transformed text data into numerical features

### 2. Dimensionality Reduction
- **PCA (Principal Component Analysis)**: Reduced dimensions from 10,000+ to 3,000 components
- **Variance Retention**: Maintained 80%+ of explained variance
- **Performance Optimization**: Prevented system crashes while preserving information

### 3. Clustering Algorithms

#### K-Means Clustering
- **Optimal K Selection**: Used Elbow Method and Silhouette Score
- **Implementation**: K-means++ initialization with random_state=42
- **Evaluation**: Silhouette analysis for cluster quality assessment

#### Hierarchical Clustering
- **Agglomerative Clustering**: Bottom-up approach
- **Dendrogram Visualization**: Tree-like structure for cluster analysis

### 4. Model Evaluation
- **Silhouette Score**: Measure of cluster cohesion and separation
- **Elbow Method**: Optimal number of clusters determination
- **Visualization**: Word clouds for cluster content analysis
- **Calinski-Harabasz Score**
- **Davies-Bouldin Score**

## Key Findings

### Data Distribution
- **Content Type**: Movies dominate the catalog (69.6%) vs TV Shows (30.4%)
- **Geographic Distribution**: United States leads content production, followed by India and UK
- **Release Years**: Content spans from 1925 to 2021, with peak additions in 2018
- **Ratings**: TV-MA (Mature Audience) is most common, followed by TV-14

### Content Analysis
- **Popular Words**: "Love", "Christmas", "Man", "World", "Life", "Girl", "Story"
- **Top Directors**: Alastair Fothergill, Jan Suter, Raúl Campos
- **Leading Actors**: Anupam Kher, Shahrukh Khan, Om Puri (Movies); Takahiro Sakurai, Yuki Kaji (TV Shows)
- **Genres**: International Movies, Dramas, and Comedies are most prevalent

### Clustering Results
- **Optimal Clusters**: Determined through multiple evaluation methods
- **Content Groupings**: Similar titles grouped based on director, cast, genre, and description
- **Recommendation Basis**: Clusters serve as foundation for content recommendations

## Technologies Used

- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Machine learning algorithms
  - KMeans clustering
  - AgglomerativeClustering
  - PCA for dimensionality reduction
  - TF-IDF vectorization
- **Matplotlib/Seaborn**: Data visualization
- **NLTK**: Natural language processing
- **WordCloud**: Cluster content visualization

## Project Structure

```
Netflix_clustering_unsupervisedML/
├── netfix_clustering.ipynb          # Main analysis notebook
├── NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv  # Dataset
├── Unsupervised_ML_netflix.pdf      # Presentation slides
└── README.md                        # Project documentation
```

## Getting Started - Replicate the Clustering Analysis

### Prerequisites

Before starting, ensure you have the following installed:

#### 1. Python Environment
```bash
# Install Python 3.8 or higher
python --version

# Create a virtual environment (recommended)
python -m venv netflix_clustering_env

# Activate virtual environment
# On Windows:
netflix_clustering_env\Scripts\activate
# On macOS/Linux:
source netflix_clustering_env/bin/activate
```

#### 2. Required Libraries
```bash
pip install -r requirements.txt
```

#### 3. Execute netflix_clustering.ipynb notebook 
