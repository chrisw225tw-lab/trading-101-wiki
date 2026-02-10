# 交易策略庫 (Strategy Library) 📚

這裡收集最經典、最經得起時間考驗的 **Trading Strategies** (交易策略)。不要小看簡單策略，複雜不代表賺錢。

## 1. 趨勢跟隨 (Trend Following) 📈

*   **核心邏輯**: "The Trend is your Friend" (趨勢是你的朋友)。如果價格在漲，就買入並持有，直到趨勢反轉。
*   **指標**: Moving Averages (MA), MACD, ADX.
*   **優點**: 一波大行情就能賺飽 (Big Wins)。
*   **缺點**: 在 **Choppy Market** (盤整市場) 會被來回停損 (Whipsaw)。

### 經典策略: 雙均線交叉 (Dual MA Crossover)
*   **規則**:
    *   **Buy**: 當 `短期 MA (e.g., 50)` 向上穿過 `長期 MA (e.g., 200)` -> **Golden Cross** (黃金交叉)。
    *   **Sell**: 當 `短期 MA` 向下穿過 `長期 MA` -> **Death Cross** (死亡交叉)。

## 2. 均值回歸 (Mean Reversion) 🔄

*   **核心邏輯**: "What goes up must come down" (漲多必跌，跌多必漲)。價格終究會回到平均值。
*   **指標**: RSI, Bollinger Bands (布林通道), Stochastic.
*   **優點**: 在盤整市場 (Range Market) 勝率很高。
*   **缺點**: 遇到強趨勢會一路逆勢攤平，直到破產 (Catching a Falling Knife)。

### 經典策略: 布林通道反彈 (Bollinger Bounce)
*   **規則**:
    *   **Buy**: 價格觸碰 `下軌 (Lower Band)` 且出現反轉 K 線。
    *   **Sell**: 價格觸碰 `上軌 (Upper Band)`。

## 3. 動能交易 (Momentum Trading) 🚀

*   **核心邏輯**: "Buy High, Sell Higher" (追高殺更高)。買入強勢股，利用市場的 **FOMO** 情緒獲利。
*   **指標**: Relative Strength (相對強度), Volume (成交量).
*   **優點**: 資金週轉快，短期爆發力強。
*   **缺點**: 需要盯盤，進出場要快狠準，滑價 (Slippage) 影響大。

### 經典策略: 突破交易 (Breakout)
*   **規則**:
    *   **Buy**: 價格突破關鍵 **Resistance** (壓力位) 且 **Volume** (成交量) 爆增。
    *   **Stop-loss**: 設在突破點下方一點點。

## 4. 套利 (Arbitrage) ⚖️

*   **核心邏輯**: "Risk-free Profit" (無風險利潤)。利用不同市場的定價錯誤 (Inefficiency)。
*   **類型**: 
    *   **Spatial**: A 交易所比特幣 $50000，B 交易所 $50100 -> A 買 B 賣。
    *   **Statistical**: 配對交易 (Pair Trading)，做多 Google 做空 Facebook。
*   **優點**: 幾乎無方向性風險 (Market Neutral)。
*   **缺點**: 利潤極薄，競爭極大 (Bot vs Bot)，需要極低的手續費和延遲。

> **Buffett 的忠告**: 
> 新手請從 **Trend Following** 開始。為什麼？因為它容錯率最高。就算你進場點爛，只要趨勢對了，還是能賺錢。Mean Reversion 需要更精準的時機。
