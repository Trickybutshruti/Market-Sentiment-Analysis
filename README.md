#Market-Sentiment-Analysis

## Project Overview

This project analyzes how trader behavior and trading performance change under different market sentiment conditions using historical trading data and the Fear & Greed Index.

Market sentiment often influences trader decisions, risk appetite, and market participation. By combining trading activity data with sentiment indicators, this analysis aims to identify patterns in profitability, trading frequency, and trading direction.

The goal of this project is to extract meaningful insights from the data and propose actionable trading strategies based on observed patterns.


## Objectives

The main objectives of this analysis are:

* Analyze trader performance under different market sentiment conditions.
* Evaluate how trading activity changes during fear and greed phases.
* Identify patterns in long and short trading behavior.
* Segment traders based on activity and performance.
* Propose actionable strategy recommendations based on the findings.


## Datasets Used

### 1. Historical Trading Data

This dataset contains detailed information about trades executed by different accounts.

Key fields include:

* Account – Unique trader identifier
* Side – Trade type (Long / Short)
* Size USD – Trade size in USD
* Closed PnL – Profit or loss from the trade
* Timestamp – Time when the trade occurred

### 2. Fear & Greed Index Dataset

This dataset represents market sentiment and classifies the market condition into categories such as:

* Fear
* Greed
* Extreme Greed
* Neutral

The sentiment data is merged with the trading dataset based on the trade date to analyze trader behavior under different market conditions.


## Methodology

The analysis was performed in several steps:

1. **Data Loading and Cleaning**

   * Imported datasets using pandas.
   * Converted timestamps into date format.
   * Handled missing values and formatted columns.

2. **Data Integration**

   * Merged trading data with sentiment data using the date column.

3. **Feature Engineering**

   * Created a **win indicator** to identify profitable trades.
   * Extracted useful metrics such as trade counts and average PnL.

4. **Performance Analysis**

   * Calculated metrics including:

     * Average PnL by sentiment
     * Win rate by sentiment
     * Trade activity by sentiment
     * Long vs short trading behavior

5. **Trader Segmentation**

   * Classified traders into:

     * Frequent vs infrequent traders
     * Consistent vs inconsistent traders

6. **Visualization**

   * Used seaborn and matplotlib to create charts illustrating key findings.


## Key Insights

1. **Market Sentiment Influences Profitability**

   Traders tend to achieve higher average profits during greed phases compared to neutral or fear periods, suggesting that optimistic market conditions may create favorable trading opportunities.

2. **Trading Activity Changes with Sentiment**

   The number of trades executed varies across sentiment conditions, indicating that trader participation and confidence are influenced by market psychology.

3. **Directional Trading Behavior**

   Traders appear to favor long positions during optimistic sentiment phases, indicating a bullish bias when market confidence is high.


## Strategy Recommendations

Based on the analysis, the following trading strategies are suggested:

**1. Increase Trading Activity During Greed Phases**

When market sentiment shifts toward greed, traders may consider increasing trading activity or position sizes to capitalize on stronger market momentum.

**2. Maintain Consistent Risk Management**

Regardless of market sentiment, traders should implement disciplined risk management practices such as stop-loss orders and controlled position sizing.

## Setup Instructions

### 1. Install Required Libraries

Run the following command to install the required Python libraries:

```
pip install pandas numpy matplotlib seaborn
```

### 2. Run the Notebook

Open the project notebook using Jupyter Notebook or VS Code and run all cells to reproduce the analysis.

```
jupyter notebook analysis.ipynb
```

## Project Structure

```
project-folder/

│
├── analysis.ipynb
├── README.md
├── fear_greed_index.csv
└── compressed_data.csv.gz
```

## Output

The notebook generates several visualizations including:

* Average PnL by market sentiment
* Win rate during fear vs greed phases
* Trade activity across sentiment categories
* Long vs short trading behavior
* Trader segmentation charts

These visualizations help illustrate how trader behavior changes under different market conditions.


## Conclusion

This project demonstrates how combining trading data with market sentiment indicators can reveal important patterns in trader behavior and performance.

Understanding how traders respond to different sentiment phases can help improve trading strategies, manage risk more effectively, and make better data-driven trading decisions.


