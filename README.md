# Give Me Some Credit - Linear Regression Analysis

使用 Kaggle [Give Me Some Credit](https://www.kaggle.com/c/GiveMeSomeCredit/) 資料集進行 **線性回歸分析**，包含：
- 單純線性回歸、多元線性回歸與 Auto Regression
- 特徵選擇 (Feature Selection)
- 模型評估 (Model Evaluation)
- 信賴區間 / 預測區間視覺化
- 依據 CRISP-DM 流程設計

---

## 🚀 CRISP-DM 流程說明

### 1️⃣ Business Understanding
目標為預測個人兩年內發生信用違約 (SeriousDlqin2yrs)，以協助金融機構預先識別高風險客戶，降低貸款損失風險。

### 2️⃣ Data Understanding
資料集包含 150,000 筆樣本、10 個特徵：
- RevolvingUtilizationOfUnsecuredLines
- age
- NumberOfTime30-59DaysPastDueNotWorse
- DebtRatio
- MonthlyIncome
- NumberOfOpenCreditLinesAndLoans
- NumberOfTimes90DaysLate
- NumberRealEstateLoansOrLines
- NumberOfTime60-89DaysPastDueNotWorse
- NumberOfDependents

### 3️⃣ Data Preparation
- 移除無用欄位 (ID)
- 以中位數補值處理缺失
- 使用 `SelectKBest(f_regression)` 進行特徵選擇，選出最具預測力的前五項變數。

### 4️⃣ Modeling
- 使用 **多元線性回歸 (Linear Regression)** 建立模型。
- 額外使用 **Auto Regression (AR)** 模型示範時間序列自動回歸。
- 模型以 80/20 分割訓練與測試資料。

### 5️⃣ Evaluation
- 指標：
  - RMSE (Root Mean Squared Error)
  - R² Score
  - Cross-Validation (5-fold)
- 可視化結果：
  - 預測 vs 實際值 散點圖
  - 預測區間 (95% Confidence Interval)

### 6️⃣ Deployment
- 將模型與程式整合為 `main.py`
- 可上傳至 GitHub
- 未來可擴展至自動化風險評估系統或整合金融信貸 API

---

## 📦 環境需求

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels

