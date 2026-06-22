# Рекомендательная система на ALS и Apache Spark

Проект реализует рекомендательную систему на основе коллаборативной фильтрации (ALS) с использованием Apache Spark. Обрабатывает 32 миллиона оценок фильмов MovieLens и генерирует персонализированные рекомендации для каждого пользователя.

## Технологии

- Apache Spark (PySpark)
- ALS (Alternating Least Squares)
- Hadoop HDFS
- Docker
- Jupyter Notebook
- FastAPI

## Запуск проекта

1. Клонировать репозиторий
2. Запустить Docker-контейнеры: `docker compose up -d`
3. Скачать данные: `python3 scripts/download_movielens.py --variant 32m`
4. Загрузить в HDFS: `bash scripts/load_to_hdfs.sh`
5. Открыть Jupyter: `http://localhost:8888`
6. Запустить `notebooks/Recommender.ipynb`

## Результаты

- **RMSE:** 0.787
- **Пользователей:** 200 948
- **Фильмов:** 23 350
- **Оценок:** 31 725 920
