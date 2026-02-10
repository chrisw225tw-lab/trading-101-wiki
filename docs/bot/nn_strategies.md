# 神經網路交易策略 (Neural Network Strategies) 🧠

歡迎來到 **AI Trading** 的深水區。這裡是用 **Neural Networks (NN)** 來預測市場，聽起來很酷，但也是大多數新手翻車的地方。

## 1. 核心概念 (Core Concept)

傳統 Bot 是用 "If-Then" 規則 (例如：MA 黃金交叉就買)。
**NN Bot** 則是餵給它海量歷史數據，讓模型自己找出規律 (Pattern)，然後預測未來的 **Price** (價格) 或 **Direction** (漲跌方向)。

*   **Input (輸入)**: 過去 30 天的 OHLCV, 技術指標, 甚至新聞情緒。
*   **Model (模型)**: 黑盒子 (Black Box)，裡面有幾百萬個參數。
*   **Output (輸出)**: 明天漲的機率是 75%。

## 2. 常見架構 (Common Architectures)

### LSTM / GRU (長短期記憶網路)
*   **原理**: 專門處理 **Time Series** (時間序列) 數據。它能"記住"很久以前的趨勢。
*   **應用**: 預測下一根 K 線的收盤價。
*   **現狀**: 經典但有點過氣。

### Transformers (變形金剛) 🤖
*   **原理**: 這是 ChatGPT 的基底架構。利用 **Attention Mechanism** (注意力機制) 找出數據中哪些部分最重要。
*   **應用**: 分析更複雜的市場結構，甚至結合新聞文本 (NLP)。
*   **現狀**: 目前的主流 (SOTA)。

### Reinforcement Learning (強化學習) 🎮
*   **原理**: 把交易當成打電動。Bot 做對了 (賺錢) 就給獎勵，做錯了 (賠錢) 就處罰。讓它自己學會怎麼玩。
*   **應用**: 自動調整倉位大小，動態止損。
*   **缺點**: 很難收斂 (Training is unstable)，容易學壞。

## 3. 開發流程 (Workflow)

1.  **Feature Engineering (特徵工程)**: 把原始價格轉成模型看得懂的訊號 (例如：RSI, Volatility)。
2.  **Training (訓練)**: 讓模型看 2010-2020 的數據學習。
3.  **Validation (驗證)**: 用 2021 的數據考考它，看它有沒有學會。
4.  **Testing (測試)**: 用 2022 的數據做最終考驗。

## 4. 致命陷阱 (The Fatal Trap)

**Overfitting (過度擬合)** 是 NN Bot 的頭號殺手。

*   **現象**: 回測績效好到爆炸 (Sharpe Ratio > 5)，但一上實盤就賠錢。
*   **原因**: 模型把歷史數據的 "雜訊" (Noise) 當成了 "規律" (Signal)。它記住了考卷答案，而不是學會了解題。
*   **解法**: 
    *   **Drop-out**: 訓練時隨機讓一些神經元休息。
    *   **Walk-forward Analysis**: 滾動式回測，模擬真實時間推進。

> **Buffett 的警告**: 
> NN Model 最大的風險是 **"Black Box" (黑箱)**。當它賠錢時，你完全不知道為什麼 (Why)。你無法 Debug 一個你看不懂的腦袋。新手請務必從簡單的邏輯回歸 (Logistic Regression) 開始，不要一上來就搞 Deep Learning。
