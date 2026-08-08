# MovieLens Recommender System

Рекомендательная система на датасете **MovieLens 100K**.  
Сравнение Item-Based Collaborative Filtering и Matrix Factorization (SVD).

## Результаты

| Метод                  | RMSE   | MAE    | Precision@10 | Recall@10 | NDCG@10 |
|------------------------|--------|--------|--------------|-----------|---------|
| Item-Based KNN         | 1.0264 | 0.8104 | 0.5594       | 0.7047    | 0.7810  |
| **SVD**                | **0.9352** | **0.7375** | **0.5837** | **0.7214** | **0.8289** |

## Что сделано

- Загрузка и анализ данных MovieLens 100K
- Item-Based Collaborative Filtering (cosine similarity)
- Matrix Factorization (SVD)
- Оценка качества: RMSE, MAE
- Ranking-метрики: Precision@10, Recall@10, NDCG@10
- Сравнение подходов

## Основные выводы

- SVD значительно превосходит Item-Based KNN как по точности оценок, так и по качеству ранжирования
- NDCG@10 у SVD достиг 0.829

## Технологии

- Python, pandas, numpy
- scikit-surprise (KNNBasic, SVD)
- scikit-learn

## Структура проекта

```text
├── notebooks/
│   └── recommender_system.ipynb
├── requirements.txt
└── README.md