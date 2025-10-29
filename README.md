# Give Me Some Credit - Linear Regression 模型分析

本專案以 Kaggle [Give Me Some Credit](https://www.kaggle.com/c/GiveMeSomeCredit/) 資料集為基礎，  
採用 **線性回歸 (Linear Regression)** 建立違約預測模型，  
包含特徵選擇、模型評估、預測區間繪製與 Kaggle 提交檔輸出。

---

## 🚀 CRISP-DM 流程說明

### 1️⃣ Business Understanding
**目標：** 預測個人在兩年內是否發生信用違約 (SeriousDlqin2yrs)。  
**意義：** 協助金融機構評估客戶信用風險、降低壞帳率。

---

### 2️⃣ Data Understanding
**資料集來源：** Kaggle 官方提供。  
包含約 150,000 筆記錄與以下欄位：
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
- SeriousDlqin2yrs (目標變數)

---

### 3️⃣ Data Preparation
- 移除 ID 欄位
- 缺失值以中位數補齊
- 使用 `SelectKBest(f_regression)` 選取 5 個最具預測力的特徵

---

### 4️⃣ Modeling
- **模型類型：** Linear Regression (多元線性回歸)  
- **特徵選擇：** SelectKBest  
- **交叉驗證：** 5-Fold CV  
- **輔助模型：** Auto Regression (示範用)

---

### 5️⃣ Evaluation
**指標：**
- RMSE (Root Mean Squared Error)
- R² (決定係數)
- Cross-Validation R² 平均
- AUC (Kaggle 評估指標)

**視覺化：**
- 實際 vs 預測值散點圖
- 95% 預測區間灰帶
- Auto Regression 預測圖

---

### 6️⃣ Deployment
- 將完整流程封裝於 `main.py`
- 執行後自動生成 `submission.csv` 可直接上傳至 Kaggle
- 未來可擴充為自動報告或信用風險 API 模型服務

---

## 📊 範例輸出

