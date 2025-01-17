# InstaCart Market Basket Analysis
<hr style="border:2px solid gray">

### 簡介

本報告的宗旨在於通過在 Kaggle 競賽中 Instacart 提供的顧客訂單數據，預測哪些曾購買過的商品會在顧客的下一次訂單中再次出現，藉此改善產品推薦系統，從而提升顧客的購物體驗和滿意度。

kaggle 競賽網址:https://www.kaggle.com/competitions/instacart-market-basket-analysis

### 核心目標

屬於二元分類問題。對於每一位顧客而言，我們需要預測每一項他們曾經購買過的產品是否會在下一份訂單中再次購買（是=1；否=0）。為了實現這一目標，我們會從顧客先前的訂單中建立多項特徵，並進行建模來預測。

# 一、數據集說明
<hr style="border:2px solid gray">

該資料集是匿名的，包含來自超過 20 萬 Instacart 用戶的 300 多萬份雜貨訂單的樣本數據。

# 二、EDA 探索性資料分析

# 三、特徵工程

# 四、建模預測

由於各個用戶的訂單特性都不盡相同，所以固定的 0 或 1 預測方法可能無法適用於所有訂單的情況。

因此我們使用 XGBoost 模型訓練，並預測每個產品被重新訂購的機率後，再根據不同的訂單調整閾值，從而獲得更好的預測效果。

### 具體的流程總結：

1. 將原先的訓練集隨機分割成測試集和驗證集 (9:1)。

2. 使用 Random search 進行超參數優化，取得最佳參數。

3. 使用最佳參數建立 XGBoost 模型，並進行訓練。

4. 使用訓練好的模型預測測試數據，獲得每個產品被重新訂購的概率。

5. 最終根據每個訂單的條件，調整閾值以最大化 F1-score。

# 推薦系統



https://github.com/KevinLin13/Instacart_Recommendation_System/assets/95026554/63732d2e-782d-4e3c-b331-2a5d52f3f995

