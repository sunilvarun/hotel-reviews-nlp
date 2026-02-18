# Hotel Reviews NLP Analysis

An NLP project analyzing the [515K Hotel Reviews Data in Europe](https://www.kaggle.com/datasets/jiashenliu/515k-hotel-reviews-data-in-europe) dataset from Kaggle, using topic modeling to identify common themes in positive and negative hotel reviews.

## Project Overview

This project preprocesses 515K hotel reviews and applies two topic modeling approaches — **LDA** (Latent Dirichlet Allocation) and **BERTopic** (transformer-based) — to discover what guests commonly praise and complain about.

## Dataset

- **Source**: Kaggle - 515K Hotel Reviews Data in Europe
- **Size**: ~515,000 reviews from 1,493 hotels
- **Features**: Hotel name, location, reviewer nationality, review scores, positive/negative review text, and more

## Project Structure

```
hotel-reviews-nlp/
├── 01_eda.ipynb                        # Exploratory data analysis
├── 02_text_preprocessing.ipynb         # Text cleaning and lemmatization with spaCy
├── 03_topic_modeling_lda.ipynb         # LDA topic modeling with Gensim
├── 04_topic_modeling_bertopic.ipynb    # BERTopic with sentence-transformers
├── data/
│   ├── Hotel_Reviews.csv              # Raw dataset (download from Kaggle)
│   ├── *_processed.parquet            # Full preprocessed data
│   └── *_sample.parquet               # 50K sample for faster iteration
├── outputs/
│   ├── models/                        # Saved LDA and BERTopic models
│   ├── topics/                        # Topic info exported as CSV
│   ├── preprocessing/                 # Gensim dictionaries
│   └── visualizations/
│       ├── wordclouds/                # Word clouds per topic (LDA + BERTopic)
│       ├── topic_distributions/       # Topic distribution charts and bar charts
│       └── intertopic_distance/       # Interactive HTML topic maps
├── requirements.txt
└── .gitignore
```

## Notebooks

Run in order:

1. **01_eda.ipynb** — Exploratory data analysis: score distributions, review lengths, nationality patterns, temporal trends
2. **02_text_preprocessing.ipynb** — Text cleaning, stopword removal, and lemmatization using spaCy's `nlp.pipe()` for batch processing. Outputs parquet files.
3. **03_topic_modeling_lda.ipynb** — LDA topic modeling with Gensim. Includes coherence score optimization, topic labeling, word clouds, and interactive pyLDAvis visualizations.
4. **04_topic_modeling_bertopic.ipynb** — BERTopic modeling with `all-MiniLM-L6-v2` sentence embeddings. Auto-discovers topics, generates interactive visualizations and word clouds.

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
   python -m spacy download en_core_web_sm
   ```
4. Download the dataset from Kaggle and place `Hotel_Reviews.csv` in the `data/` folder
5. Run notebooks in order (01 → 02 → 03 → 04)

## Key Findings

### Common Negative Themes (LDA)
- Room size and space issues
- Breakfast quality
- Noise problems
- Staff service
- Bathroom and shower issues
- Cleanliness concerns

### Common Positive Themes (LDA)
- Location and accessibility
- Friendly staff
- Room comfort
- Cleanliness
- Breakfast quality
- Value for money

BERTopic discovers similar themes with more granularity and better semantic coherence. See the notebooks for detailed results and visualizations.

## Author

Sunil

## License

MIT
