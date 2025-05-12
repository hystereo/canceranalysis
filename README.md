# Analiza przypadków raka płuc

## Cel projektu

Celem tego projektu jest zbudowanie modelu predykcyjnego, który przewiduje ryzyko wystąpienia raka płuc u pacjentów na podstawie danych medycznych. Model klasyfikacyjny ma na celu identyfikację czynników, które wpływają na wystąpienie tego schorzenia.

## Zrozumienie danych

Dane wykorzystane w projekcie pochodzą z pliku CSV zawierającego informacje o pacjentach, ich wieku, płci, stylu życia i objawach. Obejmuje to dane na temat:
- **Płeć pacjenta (GENDER)**
- **Wiek pacjenta (AGE)**
- **Czynniki i objawy (np. palenie, zmiana koloru palców, ból w klatce piersiowej, duszność)**
- **Diagnoza raka płuc (LUNG_CANCER)**

### Opis użytych narzędzi

- **Pandas** – do ładowania i manipulacji danymi.
- **Seaborn/Matplotlib** – do wizualizacji danych.
- **Sklearn** – do budowy i oceny modeli klasyfikacyjnych.
- **Imbalanced-learn (SMOTE)** – do balansowania klas w danych.

## Przygotowanie danych

Dane zostały wstępnie przetworzone poprzez:
- Mapowanie zmiennych kategorycznych na wartości numeryczne.
- Usunięcie brakujących danych.
- Standaryzację cech przy użyciu `StandardScaler`.
- Balansowanie danych za pomocą metody SMOTE w celu zrównoważenia liczby przypadków raka i braku raka.

## Modelowanie

Do stworzenia modeli klasyfikacyjnych wykorzystano następujące algorytmy:
- **Logistic Regression**
- **Random Forest**
- **LightGBM**
- **Perceptron**

Modele zostały ocenione za pomocą walidacji krzyżowej oraz metryk takich jak dokładność, macierz konfuzji i raport klasyfikacji.

## Ewaluacja

Modele zostały ocenione pod kątem ich skuteczności na danych testowych. Uzyskane wyniki:
- **Logistic Regression**: dokładność ~48%
- **Random Forest**: dokładność ~50%
- **LightGBM**: dokładność ~50%
- **Perceptron**: dokładność ~49%

## Wnioski

- Przetwarzanie i przygotowanie danych miało kluczowe znaczenie dla skuteczności modeli. 
- Zastosowanie technik takich jak standaryzacja i oversampling (SMOTE) pomogło poprawić wyniki.
- Modele klasyfikacyjne dały zbliżone wyniki, jednak w przyszłości warto rozważyć optymalizację hiperparametrów, co może poprawić dokładność.
- Warto także zbadać możliwość zastosowania bardziej zaawansowanych technik uczenia maszynowego, takich jak transfer learning, oraz wykorzystanie Big Data do dalszej analizy i predykcji w medycynie.

[Baza danych](https://www.kaggle.com/datasets/akashnath29/lung-cancer-dataset?resource=download)
