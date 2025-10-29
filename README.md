1️⃣ Business Understanding

本專案目的為建立信用風險預測模型，利用個人信貸資料（10 個特徵）預測借款人是否會於兩年內發生嚴重逾期。此分析可協助金融機構預測潛在風險、優化核貸政策。

2️⃣ Data Understanding

資料來源：Kaggle「Give Me Some Credit」競賽

樣本數：約 150,000 筆

特徵數：10 個（如收入、年齡、逾期次數等）

目標變數：SeriousDlqin2yrs (0 = 未違約, 1 = 違約)

3️⃣ Data Preparation

缺失值補齊：以中位數填補 MonthlyIncome、NumberOfDependents

標準化特徵

訓練/測試資料劃分（80/20）

4️⃣ Modeling

模型類型：多元線性回歸 (sklearn LinearRegression)

特徵選擇方法：使用遞迴特徵消除法 (RFE) 或 Lasso Regression

使用 statsmodels 建立含信賴區間的模型報表

5️⃣ Evaluation

使用 MAE、MSE、R² 進行評估

繪製預測 vs. 實際值圖

加入 95% 信賴區間與預測區間

6️⃣ Deployment

此專案可於任何 Python 環境 (>=3.9) 執行。未來可延伸為自動化信用風險預測 API 或金融儀表板。

📈 預測圖範例 (prediction_plot.png)

X 軸：實際值

Y 軸：預測值

中心線：理想預測 (y = x)

陰影部分：95% 信賴區間
