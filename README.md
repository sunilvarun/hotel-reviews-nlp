# Hotel Reviews NLP Analysis

An exploratory data analysis and NLP project using the [515K Hotel Reviews Data in Europe](https://www.kaggle.com/datasets/jiashenliu/515k-hotel-reviews-data-in-europe) dataset from Kaggle.

## Project Overview

This project analyzes hotel reviews to extract insights about customer sentiment, identify common themes, and explore patterns across different hotels and reviewer demographics.

## Dataset

- **Source**: Kaggle - 515K Hotel Reviews Data in Europe
- **Size**: ~515,000 reviews
- **Features**: Hotel name, location, reviewer nationality, review scores, positive/negative review text, and more

## Project Structure

```
hotel-reviews-nlp/
├── data/                  # Raw and processed data (not tracked in git)
├── notebooks/             # Jupyter notebooks for EDA and analysis
├── src/                   # Source code for reusable functions
├── outputs/               # Generated figures, reports, and models
├── README.md
├── requirements.txt
└── .gitignore
```

## Setup

1. Clone this repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Download the dataset from Kaggle and place `Hotel_Reviews.csv` in the `data/` folder

## Analysis Roadmap

### Phase 1: Exploratory Data Analysis
- [ ] Data quality assessment (missing values, duplicates)
- [ ] Univariate analysis of numerical features
- [ ] Review length distributions
- [ ] Geographic and temporal patterns
- [ ] Reviewer nationality analysis

### Phase 2: Text Analysis
- [ ] Text preprocessing pipeline
- [ ] Word frequency analysis
- [ ] N-gram analysis
- [ ] Word clouds for positive/negative reviews

### Phase 3: Sentiment & Topic Modeling
- [ ] Sentiment analysis validation against scores
- [ ] Topic modeling (LDA/BERTopic)
- [ ] Key phrase extraction

### Phase 4: Predictive Modeling (Optional)
- [ ] Review score prediction from text
- [ ] Classification of review sentiment

## Key Questions to Explore

1. What are the most common complaints and praises?
2. How do review patterns differ by reviewer nationality?
3. Are there seasonal patterns in review sentiment?
4. Which hotels consistently outperform/underperform?
5. What text features best predict review scores?

## Author

Sunil

## License

MIT
