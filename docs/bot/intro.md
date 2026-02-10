# 程式交易入門 (Bot Trading 101) 🤖

歡迎來到 **Bot Trading** (程式交易/量化交易) 的世界。這裡不是教你寫 code，而是教你如何 **Design** (設計) 和 **Manage** (管理) 一個交易機器人。

## 1. 為什麼要用 Bot? (Why Bot?)

*   **Emotionless Execution (無情緒執行)**: 機器人不會因為恐懼而不敢下單，也不會因為貪婪而 **FOMO** (錯失恐懼)。
*   **Consistency (一致性)**: 只要規則設定好，它會 100% 嚴格執行，不會累、不會睡。
*   **Speed (速度)**: 它可以 24/7 監控幾百個 **Tickers** (標的)，人類做不到。

## 2. 核心組件 (Key Components)

一個完整的 Bot 系統通常包含四個部分：

1.  **Data Feed (數據源)**
    *   機器人的眼睛。例如：價格 (Price)、成交量 (Volume)、訂單簿 (Order Book)。
    *   *重點*：**Data Quality** (數據品質) 決定一切。垃圾進，垃圾出 (GIGO)。

2.  **Strategy Engine (策略引擎)**
    *   機器人的大腦。負責計算訊號 (Signal)：
        *   **Entry Signal**: 什麼時候買？(e.g., MA Cross)
        *   **Exit Signal**: 什麼時候賣？(e.g., Stop-loss, Take Profit)

3.  **Execution System (執行系統)**
    *   機器人的手。負責把訊號變成訂單 (Order) 發送給 **Exchange** (交易所)。
    *   *重點*：要處理 **Slippage** (滑價) 和 **Latency** (延遲)。

4.  **Risk Management (風控模組)**
    *   機器人的安全帶。
    *   *絕對規則*：在發送訂單前，必須檢查是否超過 **Max Drawdown** (最大回撤) 或 **Position Limit** (倉位限制)。

## 3. 開發流程 (Development Workflow)

不要一開始就上 **Live** (實盤)！請遵守標準流程：

1.  **Backtesting (回測)** 🧪
    *   用 **Historical Data** (歷史數據) 跑策略。
    *   *陷阱*：**Overfitting** (過度擬合) — 為了讓過去績效好看而硬湊參數，未來一定死很慘。

2.  **Paper Trading (模擬交易)** 📝
    *   接即時數據，但不花真錢。
    *   測試 **Infrastructure** (基礎設施) 穩不穩，有沒有 Bug。

3.  **Live Trading (實盤交易)** 💸
    *   **Small Size** (小資金) 開始。
    *   監控 **PnL** (損益) 和 **Logs** (日誌)。

## 4. 常見陷阱 (Common Pitfalls)

*   **Look-ahead Bias (偷看未來)**: 回測時用到了當時還不知道的數據 (例如用當天收盤價去決定當天開盤買不買)。
*   **Survivorship Bias (倖存者偏差)**: 只測試現在還活著的公司，忽略了已經下市的爛股。
*   **Ignored Costs (忽略成本)**: 沒把 **Commission** (手續費) 和 **Slippage** (滑價) 算進去，結果回測賺錢，實盤賠錢。

> **Buffett 的忠告**: 
> Bot 是一個 **Tool** (工具)，不是 ATM。你必須比它更懂交易，才能駕馭它。
