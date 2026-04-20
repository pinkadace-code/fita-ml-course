# TMDb Filmu Vērtējuma Prognozēšana

## Problēma
Prognozējam, vai filma tiks augsti novērtēta (vote_average > 6.5),
izmantojot klasifikācijas modeli ar TMDb populāro filmu datiem.

## Datasets
- Avots: [TMDb Top 10,000 Popular Movies Dataset (Kaggle)](https://www.kaggle.com/datasets/balaka18/tmdb-top-10000-popular-movies-dataset)
- Izmērs: 9804 rindas × 6 kolonnas (pēc tīrīšanas)
- Target kolonna: high_rating (1 = vote_average > 6.5, 0 = nē)

## Pieeja
- ML tips: Klasifikācija
- Pipeline: SimpleImputer → StandardScaler → LogisticRegression
- Optimizācija: GridSearchCV (C, max_iter, solver)

## Rezultāti
- Bāzes modelis: CV F1 = 0.4392
- Labākais modelis: CV F1 = 0.6042 (uzlabojums: +37.6%)
- Galvenās pazīmes: year, lang_en, vote_count

## Kā palaist
1. `pip install -r requirements.txt`
2. Atver `week4_homework.ipynb`
3. Izpildi visas šūnas (Kernel → Restart & Run All)

## Autors
Tavs vārds, FITA ML kurss, 2025
