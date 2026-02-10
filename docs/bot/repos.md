# 熱門交易機器人庫 (Top Trading Bot Repos) 🏆

工欲善其事，必先利其器。這裡列出 GitHub 上最受歡迎、經過社群驗證的 **Open Source** (開源) 交易框架。

## 1. Freqtrade (Crypto King) 👑

*   **專注領域**: **Cryptocurrency** (加密貨幣)
*   **語言**: Python
*   **Repo**: [freqtrade/freqtrade](https://github.com/freqtrade/freqtrade)

### 為什麼好? (Why Good?)
1.  **All-in-One**: 從 **Downloader** (下載數據)、**Backtesting** (回測)、**Hyperopt** (參數優化) 到 **Live Trading** (實盤)，一條龍全包。
2.  **Safety First**: 內建很強的 **Stoploss** (止損) 和 **ROI** (止盈) 機制，還有 **Trailing Stop** (移動止損)。
3.  **Telegram Integration**: 直接用 Telegram 控制機器人，隨時隨地監控。
4.  **Community**: 社群非常活躍，有很多現成的策略可以參考 (但小心 **Overfitting**)。

> **Buffett 評語**: 新手想做 Crypto Bot 的首選。但千萬別用預設策略直接上實盤，保證賠光。

---

## 2. Backtrader (Strategy Lab) 🧪

*   **專注領域**: **Backtesting** (回測) & 通用交易
*   **語言**: Python
*   **Repo**: [mementum/backtrader](https://github.com/mementum/backtrader)

### 為什麼好? (Why Good?)
1.  **Flexibility**: 寫策略的邏輯非常像真實交易 (Event-driven)。
2.  **Visual**: 內建 **Plotting** (繪圖) 功能，回測完直接畫圖給你看進出場點，除錯神器。
3.  **Broker Agnostic**: 同一套邏輯可以接 Interactive Brokers (股票)、Oanda (外匯) 或 Crypto 交易所。

> **Buffett 評語**: 這是「學交易邏輯」最好的地方。先在這裡把策略磨利，再去考慮自動化。

---

## 3. Lean (The Pro Engine) 🏢

*   **專注領域**: **Quant** (量化) & 多資產 (股票/期貨/外匯/Crypto)
*   **語言**: C# (核心), Python (支援)
*   **Repo**: [QuantConnect/Lean](https://github.com/QuantConnect/Lean)

### 為什麼好? (Why Good?)
1.  **Institutional Grade**: 這是 **QuantConnect** 平台背後的引擎，設計架構是機構等級的。
2.  **Data Quality**: 處理 **Corporate Actions** (除權息、拆股) 和 **Ticks** (逐筆數據) 非常嚴謹。
3.  **Reality Check**: 模型非常貼近真實市場，包含 **Slippage** (滑價) 和 **Market Impact** (市場衝擊) 模型。

> **Buffett 評語**: 如果你想做正規軍 (Hedge Fund 風格)，學這個。但學習曲線很陡峭 (Hardcore)。

---

## 4. Hummingbot (Market Maker) 💧

*   **專注領域**: **Market Making** (造市) & Arbitrage (套利)
*   **語言**: Python / Cython
*   **Repo**: [hummingbot/hummingbot](https://github.com/hummingbot/hummingbot)

### 為什麼好? (Why Good?)
1.  **Niche Focus**: 專門做 **Liquidity Provision** (提供流動性)，不是做方向性交易 (Directional Trading)。
2.  **Exchange Incentives**: 很多小交易所會付錢 (Rebate) 給你讓你去掛單，這是另一種獲利模式。
3.  **Connector**: 支援超多去中心化交易所 (DEX) 和中心化交易所 (CEX)。

> **Buffett 評語**: 造市是撿芝麻的遊戲，風險在於 **Inventory Risk** (庫存風險)。新手慎入，除非你很懂訂單簿 (Order Book)。
