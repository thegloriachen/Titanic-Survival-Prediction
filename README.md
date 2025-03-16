# Titanic Survival Prediction

## 📌 專案介紹
本專案基於 Kaggle Titanic 資料集，目標為預測乘客在鐵達尼號沉船事故中的生存機率。透過資料清理與特徵工程，搭配機器學習模型進行預測分析。

## 🔧 使用技術
- Python (Pandas)
- 機器學習：Scikit-learn (ensemble.RandomForestClassifier)

## 💻Project Source Codes:
[Titanic Survival Prediction](https://github.com/thegloriachen/Titanic-Survival-Prediction/blob/main/Titanic-Survival-Prediction.py)

## 🚀 分析流程

### 1. 資料預處理（Data Preprocessing）
- 將訓練與測試資料集的缺失值進行處理  
  - `Age` 與 `Fare` 欄位以中位數補值  
  - `Embarked` 欄位缺失以 'S' 進行補值  
- 類別資料轉換  
  - `Sex` 欄位：'male' ➜ 1，'female' ➜ 0  
  - `Embarked` 欄位：'S' ➜ 0，'C' ➜ 1，'Q' ➜ 2

### 2. 特徵選擇（Feature Selection）
挑選影響生存率的特徵欄位作為模型輸入：
- `Pclass`  
- `Age`  
- `Sex`  
- `SibSp`  
- `Parch`  
- `Fare`  
- `Embarked`

### 3. 模型建置（Model Training）
- 使用 `RandomForestClassifier` 進行模型訓練  
- 超參數設定：  
  - `max_depth=5`  
  - `min_samples_leaf=6`  
- 訓練集上模型準確率輸出（Training ACC）

### 4. 測試與預測（Prediction & Output）
- 對測試集資料進行預測  
- 預測結果依照 Kaggle 標準格式輸出至 `forest.csv`  
