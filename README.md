# Dissertation
Evaluating AI-Driven Product Recommendation Systems

Project Overview

This project presents a comparative evaluation of two content-based product recommendation approaches using Amazon Fashion customer reviews:

- TF-IDF with Cosine Similarity
- Transformer-based Semantic Embeddings

The study investigates how different text-representation techniques affect recommendation relevance, ranking quality, catalogue coverage and recommendation diversity.

Dataset

The project uses the Amazon Fashion Customer Reviews Dataset.

Dataset source:
https://www.kaggle.com/datasets/fawadhossaini1415/amazon-fashion-800k-user-reviews-dataset

The final analysis contained 865,852 cleaned reviews representing 424,283 unique products.

Methodology

Customer reviews are aggregated at product level to create a textual representation for each product. Two recommendation approaches are then implemented using the same product representations and evaluation framework.

1. TF-IDF Recommendation

TF-IDF is used to convert product review text into numerical representations. Cosine similarity is then used to identify and rank similar products.

2. Transformer Recommendation

A transformer-based semantic embedding approach is used to capture contextual relationships within product review text.

The experiment uses:

"sentence-transformers/all-MiniLM-L6-v2"

The resulting product embeddings contain 384 dimensions.

Evaluation Metrics

Both approaches are evaluated using:

- Precision@5, @10 and @20
- Recall@5, @10 and @20
- NDCG@5, @10 and @20
- Catalogue Coverage
- Recommendation Diversity

A rating-based offline relevance criterion is used because the dataset does not contain recommendation exposure, click or purchase information.

Consumer Evaluation

A secondary analysis investigates customer ratings and rating-derived sentiment.

Ratings are grouped as:

- 1–2: Negative
- 3: Neutral
- 4–5: Positive

The analysis also considers review length, helpful votes and verified purchase information.

Key Results

The experimental results showed that TF-IDF achieved higher Precision@K and NDCG@K across the evaluated recommendation cut-offs.



The results demonstrate that greater model complexity does not automatically lead to better recommendation performance under the study's evaluation framework.

Research Questions

The project addresses the following questions:

1. How effectively can Amazon Fashion customer review text generate content-based recommendations?
2. Does the transformer approach produce different recommendation relevance from TF-IDF?
3. How do the approaches differ in Precision@K, Recall@K and NDCG@K?
4. How do they differ in catalogue coverage and recommendation diversity?
5. What relationships exist between customer ratings, rating-derived sentiment and review characteristics?

Limitations

The study is based on offline evaluation and does not include real customer clicks, purchases or recommendation exposure. It also uses a single transformer model and Amazon Fashion data, which limits generalisation to other domains.

Conclusion

This project provides a controlled comparison of lexical and semantic text representations for content-based product recommendation. It demonstrates how customer review data can be transformed into product representations and evaluated using multiple recommendation-quality measures.
