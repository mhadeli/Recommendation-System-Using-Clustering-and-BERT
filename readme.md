# Recommendation System Using Clustering and BERT

A Python-powered system for automatically categorizing and recommending Massive Open Online Courses (MOOCs) using advanced NLP techniques and clustering algorithms.

<img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMSkillsNetwork-GPXX0QZ9EN/images/course%20recommendation.png" alt="clustering courses">

## Overview

This project addresses the challenge of organizing and recommending courses in a MOOC platform where hundreds of new courses are created daily. Using course descriptions as input, the system automatically:
- Identifies natural course specializations through clustering
- Assigns courses to appropriate specializations
- Recommends similar courses based on content

## Table of Contents

1. [Features](#features)
2. [Technical Details](#technical-details)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Data Processing Pipeline](#data-processing-pipeline)
6. [Methodology](#methodology)
7. [Results](#results)
8. [Project Structure](#project-structure)

## Features

- Automated course categorization using state-of-the-art NLP models
- Dynamic specialization discovery through clustering
- Content-based course recommendations
- Interactive visualization of course relationships
- Scalable processing pipeline for large course catalogs

## Technical Details

### Technologies Used

- **Python 3.8+**
- **Key Libraries**:
  - sentence-transformers (BERT embeddings)
  - scikit-learn (clustering)
  - pandas (data processing)
  - plotly (visualization)

### Core Components

- BERT-based text vectorization
- K-means clustering for specialization discovery
- Optimization algorithms for cluster number selection
- Distance-based recommendation engine

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/course-recommendation-system.git

# Install dependencies
pip install -r requirements.txt
```

## Usage

```python
from course_recommender import CourseRecommender

# Initialize the recommender
recommender = CourseRecommender()

# Train on your course catalog
recommender.train('course_catalog.csv')

# Get recommendations
similar_courses = recommender.recommend('python programming')
```

## Data Processing Pipeline

1. **Text Preprocessing**
   - Lowercase conversion
   - Punctuation removal
   - Stop word elimination
   - Lemmatization

2. **Feature Extraction**
   - BERT sentence embeddings
   - Dimensionality reduction
   - Feature normalization

3. **Cluster Analysis**
   - Optimal cluster number determination
   - K-means clustering
   - Cluster validation

## Methodology

### Text Vectorization

The system uses Sentence-BERT (SBERT) for converting course descriptions into high-dimensional vectors, enabling:
- Semantic similarity comparison
- Content-based clustering
- Efficient similarity search

### Clustering Optimization

Multiple methods are employed to determine the optimal number of clusters:
- Elbow method
- Silhouette analysis
- Calinski-Harabasz index
- Davies-Bouldin index

### Course Assignment

Courses are assigned to specializations using:
1. Vector similarity measures
2. Cluster membership
3. Distance-based metrics

## Results

The system achieves:
- Accurate specialization identification
- Coherent course groupings
- Fast recommendation generation
- Scalable processing of large course catalogs


## Data Source

The course catalog dataset is sourced from the University of Illinois and includes:
- Course descriptions
- Subject codes
- Credit hours
- Term information
- Degree attributes

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Acknowledgments

- University of Illinois for the course catalog dataset
- Sentence-Transformers team for the BERT implementation
- Contributors and maintainers of key dependencies

## Contact

Hussain Adeli - [@yourusername](https://github.com/mhadeli)
