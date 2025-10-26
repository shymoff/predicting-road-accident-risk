# Predykcja ryzyka wypadków drogowych (Kaggle Playground Series S5E10)

Projekt koncentruje się na **predykcji ryzyka wypadków drogowych** z wykorzystaniem modeli uczenia maszynowego typu ensemble, trenowanych na połączonych zbiorach danych rzeczywistych i syntetycznych.  
Celem jest minimalizacja **Root Mean Squared Error (RMSE)** na publicznym leaderboardzie Kaggle.

---

## 🧠 Opis projektu

- **Konkurs:** [Kaggle Playground Series S5E10](https://www.kaggle.com/competitions/playground-series-s5e10)  
- **Cel:** Predykcja prawdopodobieństwa (`accident_risk`) wystąpienia wypadku drogowego w zależności od warunków środowiskowych i ruchu drogowego.  
- **Wynik:** RMSE = **0.05559**, co plasuje projekt w **górnych 33% uczestników** na publicznym leaderboardzie.  
- **Podejście:** Połączenie wyników trzech modeli boostingowych w **ensemble**, uśrednienie predykcji dla większej stabilności.

---

## ⚙️ Technologie i narzędzia

- **Język:** Python (pandas, numpy, scikit-learn)  
- **Modele:** LightGBM, XGBoost, CatBoost  
- **Walidacja:** 5-krotna walidacja krzyżowa (KFold)  
- **Środowisko:** Kaggle Notebooks / Jupyter  
- **Metryka:** Root Mean Squared Error (RMSE)  

---

## 🧩 Metodyka

1. **Przygotowanie danych**
   - Połączenie zbiorów danych rzeczywistych i syntetycznych  
   - Kodowanie zmiennych kategorycznych (one-hot encoding)  
   - Usunięcie nieistotnych kolumn, np. `id`  

2. **Modelowanie**
   - Trenowanie trzech modeli boostingowych:  
     - `LGBMRegressor`  
     - `XGBRegressor`  
     - `CatBoostRegressor`  
   - Zastosowanie **5-krotnej walidacji KFold**  
   - Uśrednianie wyników modeli w celu poprawy stabilności predykcji  

3. **Ewaluacja**
   - Obliczenie RMSE dla każdego folda  
   - Uśrednienie predykcji dla zbioru testowego  

---

## 📊 Wyniki

- **RMSE:** 0.05559  
- **Public Leaderboard:** Top 33%  
