# Recommendation System: IBM Watson Studio Community

Recommendation engines for articles on the IBM Watson Studio platform, built
from 45,993 real user-article interactions (5,149 users, 714 articles). The
project implements and compares four approaches, from simple to sophisticated,
and discusses how each should be deployed and evaluated.

## What's inside

| Part | Method | Purpose |
|---|---|---|
| I | Exploratory data analysis | Understand users, articles and interaction patterns |
| II | Rank-based recommendations | Most-popular articles; the cold start answer for new users |
| III | User-user collaborative filtering | Personalised recommendations from similar users (cosine similarity), improved with interaction-count ranking |
| IV | Content-based recommendations | TF-IDF + LSA + KMeans clustering of article titles to recommend topically similar articles |
| V | Matrix factorisation (SVD) | Latent-feature decomposition of the user-item matrix and article-article similarity via cosine distance |

The notebook ends with a discussion of latent-feature selection, the limits of
offline evaluation on this data, and a concrete A/B testing design for
measuring the recommender in production.

## Getting Started

### Dependencies

```
Python 3.10+
pandas
numpy
matplotlib
scikit-learn
jupyter
```

### Installation

```
git clone <your fork URL>
cd dsnd-recommendation-systems-project
pip install pandas numpy matplotlib scikit-learn jupyter
jupyter notebook starter/Recommendations_with_IBM.ipynb
```

Run all cells top to bottom. All built-in tests (`project_tests.py`) and
asserts pass; fixed random seeds make the results reproducible.

## Files

| Path | Description |
|---|---|
| `starter/Recommendations_with_IBM.ipynb` | Completed project notebook |
| `starter/data/user-item-interactions.csv` | User-article interaction data |
| `starter/project_tests.py` | Provided test suite used throughout the notebook |
| `starter/top_5.p`, `top_10.p`, `top_20.p` | Provided solution pickles for the rank-based tests |

## Acknowledgements

Data and project structure provided by Udacity in partnership with IBM Watson Studio.

## License

[License](LICENSE.txt)
