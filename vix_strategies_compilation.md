# VIX Trading Strategies - Complete Compilation

## Strategy 1: Godot Finance's Mojito 3.0 Strategy

### Rules
- Calculate IVTS = VIX spot / 45-day constant maturity price of VIX futures
- Calculate 5-day median value of IVTS
- **Long XIV** when 5-day median IVTS < 0.91
- **Long VXX** when 5-day median IVTS > 1.10
- **Cash** when 5-day median IVTS between 0.91 and 1.10
- Hold until change in position

### Inputs Required
- VIX spot price
- VIX futures (1st and 2nd month for 45-day constant maturity calculation)
- 5-day median calculation

### Traded Instruments
- **XIV** (Short Vol) - when term structure compressed
- **VXX** (Long Vol) - when term structure inverted
- **Cash** - when in neutral zone

### Performance
- Not explicitly stated in document
- Chart shows significant outperformance vs Buy & Hold XIV from 2004-2015

### Notes
- 45-day constant maturity uses weighted average of 1st/2nd month futures (if 2nd month >45 days) or 2nd/3rd month futures (if 2nd month ≤45 days)

---

## Strategy 2: TTO's "Trading the Odds" Optimized VRP Strategy

### Rules
- Calculate: 5-day EMA of [30-day constant maturity VIX futures - (2-day historical volatility of SPY × 100)]
- **Long XIV** when result > 1
- **Long VXX** when result ≤ 1
- Hold until change in position

### Inputs Required
- 30-day constant maturity VIX futures price
- SPY 2-day historical volatility
- 5-day exponential moving average

### Traded Instruments
- **XIV** (Short Vol) - when volatility risk premium positive
- **VXX** (Long Vol) - when volatility risk premium negative

### Performance
- Uses 30-day constant maturity futures (not VIX spot)
- Uses EMA (not simple MA) for more responsiveness
- Performance worse than TTO's published results due to using SPY vs GSPC

### Notes
- Author transparent about backtest differences vs original
- Emphasizes overfitting concerns

---

## Strategy 3: VRP Strategy with Different Averages (Original)

### Rules
- **Long XIV:** 5-day average of [VIX - (2-day historical volatility of S&P 500 × 100)] > 0
- **Long VXX:** 5-day average of [VIX - (2-day historical volatility of S&P 500 × 100)] ≤ 0
- Hold until change in position
- Always market on close

### Inputs Required
- VIX spot price
- S&P 500 2-day historical volatility
- 5-day moving average (type varies)

### Traded Instruments
- **XIV** (Short Vol) - when VRP positive
- **VXX** (Long Vol) - when VRP zero or negative

### Performance
- Chart compares different average types: IDWMA, DWMA, SMA, EMA
- Best performer: EMA using VX1|VX2 contracts with threshold of 1 instead of 0
- Reaches towards $1 billion from $1,000 starting capital
- Not adaptive - always all-in, no filters

### Notes
- Tests different smoothing methods
- Green line (IDWMA with VX contracts) showed exponential growth
- Strategy does NOT adjust for market conditions or use filters

---

## Strategy 4: Ilya's QuantStrat TradeR Strategy (Combined Parameters)

### Rules
- Calculate ratio: VXV (3-month VIX) / VXMT (mid-term VIX)
- Calculate 60-day, 125-day, and 150-day averages of this ratio
- For each timeframe:
  - **Short vol** if ratio < average AND average < 1
  - **Long vol** if ratio > average AND average > 1
  - Otherwise cash
- Average signals from all 3 timeframes (e.g., 2 short + 1 cash = 2/3 position short vol)
- Execute signal next day's close (1-day lag)
- Hold until change

### Inputs Required
- VXV (3-month VIX / 93-day implied volatility)
- VXMT (mid-term VIX)
- 60-day, 125-day, 150-day moving averages

### Traded Instruments
- **XIV** (Short Vol) - fractional positions possible
- **VXX** (Long Vol) - fractional positions possible
- **Cash** - fractional positions possible

### Performance (08/2008 to Present)
- **Annualized Return:** 64.0% vs 19.7% (Buy & Hold)
- **Sharpe Ratio:** 1.89 vs 0.27
- **Max Drawdown:** -32.5% vs -81.7%
- **Ulcer Performance Index:** 5.75 vs 0.48
- **Correlation with S&P 500:** 10.9% vs 76.8%
- **Best Month:** 35.3%
- **Worst Month:** -15.8%
- **% Winning Months:** 61.6%
- **Days in Market:** 64.8%
- **Trades per Year:** 53.4

### Notes
- Combines 3 different parameter values into one strategy
- Uses fractional position sizing
- 1-day execution lag

---

## Strategy 5: Macro Investor Strategy (VMS Version)

### Rules
- Calculate R = [average of (VX1/VIX, VX2/VX1) - 1]
- Calculate average R from inception to current date (expanding window)
- **Long XIV** if R > (average historical R × -1)
- **Long VXX** otherwise
- Hold until change in position

### Inputs Required
- VIX spot
- VX1 (first month VIX futures)
- VX2 (second month VIX futures)
- Expanding window average of R from inception

### Traded Instruments
- **XIV** (Short Vol) - when current term structure better than historical average
- **VXX** (Long Vol) - when current term structure worse than historical average

### Performance (07/2004 to 11/2014)
- **Annualized Return:** 78.2% vs 29.3% (Buy & Hold)
- **Sharpe Ratio:** 1.34 vs 0.43
- **Max Drawdown:** -80.1% vs -91.9%
- **Ulcer Performance Index:** 2.73 vs 0.60

### Notes
- Different from Macro Investor's original (which used UVXY - 2x leveraged)
- Original only spent 6% of days long VIX (high overfitting risk)
- Author version more conservative

---

## Strategy 6: New SVXY Strategy (Macro Investor/Seeking Alpha)

### Rules
- Step 1: R = average(F1/V, F2/F1) - 1
- Step 2: Calculate average R from inception to date
- Step 3: **Invest in SVXY** if current R > -1 × average historical R
- Step 3: **Invest in UVXY** otherwise

### Inputs Required
- V = VIX spot
- F1 = first month VIX future
- F2 = second month VIX future
- Historical average R (expanding window)

### Traded Instruments
- **SVXY** (Short Vol) - 94% of time
- **UVXY** (Long Vol) - 6% of time

### Performance (2004-2014)
- **Average Annual Return:** ~100% vs ~35% for holding SVXY alone
- **Historical R value:** Currently 4.8% (ranged 3.4% to 11.3%)
- **Max Drawdown:** -85%+ during 2007-2008 crash (SVXY crashed 90%)

### Notes
- Uses simulated SVXY from VIX futures
- Despite high returns, still has deep drawdowns
- Very asymmetric allocation (94% short vol, 6% long vol)

---

## Strategy 7: MarketSci's Mean-Reversion Filter

### Rules
- **When base strategy signals short vol (XIV)** AND **10-day EMA of VIX > 10-day SMA of VIX**: Go long XIV
- **When base strategy signals long vol (VXX)** AND **10-day EMA of VIX < 10-day SMA of VIX**: Go long VXX
- **Otherwise:** Cash
- Hold until change in position

### Inputs Required
- Base strategy signal (any VRP strategy)
- VIX 10-day EMA
- VIX 10-day SMA

### Traded Instruments
- **XIV** (Short Vol) - only when VIX is overbought (EMA > SMA)
- **VXX** (Long Vol) - only when VIX is oversold (EMA < SMA)
- **Cash** - when filter disagrees with base signal

### Performance
- Chart shows filtered trades (blue) significantly outperform unfiltered (grey)
- Filter meant to work WITH existing longer-term strategy
- Successfully avoids many drawdown periods

### Notes
- This is a FILTER, not standalone strategy
- EMA faster than SMA = mean-reversion approach
- Only takes short vol when VIX overbought, long vol when VIX oversold

---

## Strategy 8: TTO's Strategy (Revised with 1.25 Threshold)

### Rules
- Calculate: 5-day average of [VIX index - (2-day historical volatility of SPY × 100)]
- Note: historical volatility based on natural log of each day's % change
- **Long XIV** when result > 1.25
- **Long VXX** when result ≤ 1.25
- Hold until change in position

### Inputs Required
- VIX spot price
- SPY 2-day historical volatility (log returns)
- 5-day simple moving average

### Traded Instruments
- **XIV** (Short Vol) - when VRP exceeds 1.25 threshold
- **VXX** (Long Vol) - when VRP at or below 1.25

### Performance (07/2004 to Present)
- **Annualized Return:** 83.0% vs 28.4% (Buy & Hold)
- **Sharpe Ratio:** 1.62 vs 0.42
- **Max Drawdown:** -65.2% vs -91.9%
- **Ulcer Performance Index:** 3.49 vs 0.58
- **Correlation with S&P 500:** 29.4% vs 75.8%
- **Best Month:** 100.2%
- **Worst Month:** -32.3%
- **% Winning Months:** 66.1%
- **Days in Market:** 100.0%
- **Trades per Year:** 22.0

### Notes
- Uses natural log for volatility calculation
- 1.25 threshold instead of 0 or 1
- Compared favorably with Brute Force VRP strategy

---

## Strategy 9: Brute Force VRP Strategy

### Rules
- Similar to TTO's but different threshold/smoothing
- **Long XIV** when volatility risk premium positive (threshold not specified as 1.25)
- **Long VXX** otherwise
- Hold until change in position

### Inputs Required
- VIX index
- SPY historical volatility
- Moving average (type/period not fully specified)

### Traded Instruments
- **XIV** (Short Vol)
- **VXX** (Long Vol)

### Performance (07/2004 to Present)
- **Annualized Return:** 105.0% vs 28.4% (Buy & Hold)
- **Sharpe Ratio:** 1.93 vs 0.42
- **Max Drawdown:** -52.1% vs -91.9%
- **Ulcer Performance Index:** 5.77 vs 0.58
- **Correlation with S&P 500:** 13.8% vs 75.8%
- **Best Month:** 139.2%
- **Worst Month:** -30.4%
- **% Winning Months:** 67.7%
- **Days in Market:** 100.0%
- **Trades per Year:** 7.4

### Notes
- Higher returns than TTO's (105% vs 83%)
- Better max drawdown (-52.1% vs -65.2%)
- Much lower trading frequency (7.4 vs 22.0 trades/year)
- Author says both strategies similar enough to be equally confident

---

## Strategy 10: Simple VIX/VXV Strategy

### Rules
- **Long XIV** if VIX index will close below VXV index
- **Long VXX** if VIX will close above VXV
- Hold until change in position

### Inputs Required
- VIX (30-day implied volatility)
- VXV (93-day / 3-month implied volatility)

### Traded Instruments
- **XIV** (Short Vol) - when term structure in contango
- **VXX** (Long Vol) - when term structure in backwardation

### Performance
- Chart shows strong outperformance vs Buy & Hold XIV from mid-2004 to present
- Specific metrics not provided

### Notes
- Simplest strategy presented (single comparison)
- VIX < VXV = contango (normal state)
- VIX > VXV = backwardation (fear/stress state)

---

## Strategy 11: VIX vs 1-Month Constant Maturity Strategy

### Rules
- **Long XIV** if VIX index will close below 1-month constant maturity price of VIX futures
- **Long VXX** if VIX will close above 1-month constant maturity
- Hold until change in position

### Inputs Required
- VIX spot price
- 1-month constant maturity VIX futures (weighted average of VX1 and VX2)

### Traded Instruments
- **XIV** (Short Vol) - when VIX below 1-month futures (contango)
- **VXX** (Long Vol) - when VIX above 1-month futures (backwardation)

### Performance
- Chart shows massive outperformance vs Buy & Hold XIV from mid-2004 to present
- Especially strong post-2009

### Notes
- 1-month constant maturity = mix of 1st/2nd month futures achieving 1-month weighted average
- Similar logic to VIX/VXV but uses futures instead of VXV index

---

## Strategy 12: VRP Strategy (Original - 10-day lookback)

### Rules
- **Long XIV:** 5-day average of [VIX index - (10-day historical volatility of SPY × 100)] > 0
- **Long VXX:** 5-day average of [VIX index - (10-day historical volatility of SPY × 100)] < 0
- Hold until change in position

### Inputs Required
- VIX spot price
- SPY 10-day historical volatility
- 5-day simple moving average

### Traded Instruments
- **XIV** (Short Vol) - when VRP positive
- **VXX** (Long Vol) - when VRP negative

### Performance
- Delivered extraordinary results 2004-2012
- Issues identified during VIX spikes (10-day lookback too slow)

### Notes
- Original version before revision to 2-day lookback
- Problems: (1) Uses VIX data instead of VIX futures, (2) 10-day timeframe too slow for sudden changes

---

## Strategy 13: Revised VRP Strategy (2-day lookback, 1.25 threshold)

### Rules
- **Long XIV:** 5-day average of [VIX index - (2-day historical volatility of S&P 500 × 100)] > 1.25
- **Long VXX:** 5-day average of [VIX index - (2-day historical volatility of S&P 500 × 100)] < 1.25
- Hold until change in position

### Inputs Required
- VIX spot price
- S&P 500 2-day historical volatility
- 5-day simple moving average

### Traded Instruments
- **XIV** (Short Vol) - when VRP exceeds 1.25
- **VXX** (Long Vol) - when VRP below 1.25

### Performance (03/25/2004 - 10/15/2014)
- Chart shows growth to $24,122,940.75
- Both revised and original (10-day) versions tracked closely
- Dramatic outperformance vs Buy & Hold XIV

### Notes
- Changed from 10-day to 2-day for responsiveness
- Added 1.25 threshold (buffer/premium) instead of 0
- More responsive to sudden volatility changes

---

## Strategy 14: Evolution Capital's Combined VIX ETP Strategy

### Rules

**Long VXX when:**
- VIX closes above VX1 (front month futures) AND
- VX1 closes above VX2 (second month futures)
- (VIX > VX1 > VX2)

**Long XIV when ALL of:**
- VIX closes below VX1 AND
- VX1 closes below VX2 AND
- Current roll yield > 20-day average roll yield
- (VIX < VX1 < VX2 and RY > 20-day RY)

**Cash when:**
- Strategy signals long XIV BUT
- Both SPY and VX1 close up on the day (unusual divergence)
- Or when none of the above conditions met

### Inputs Required
- VIX spot
- VX1 (first month VIX futures)
- VX2 (second month VIX futures)
- SPY daily change
- Roll yield and 20-day average

### Traded Instruments
- **XIV** (Short Vol) - when term structure normal and roll yield favorable
- **VXX** (Long Vol) - when term structure inverted
- **Cash** - during unusual market divergences

### Performance (07/2004 to Present)
- **Annualized Return:** 44.3% vs 27.5% (Buy & Hold)
- **Sharpe Ratio:** 0.94 vs 0.40
- **Max Drawdown:** -74.9% vs -91.9%
- **Ulcer Performance Index:** 1.67 vs 0.56
- **Correlation with S&P 500:** -16.3% vs 75.9%

### Notes
- ONLY strategy with negative S&P 500 correlation (-16.3%)
- Uses roll yield explicitly
- Cash filter for SPY/VX1 divergence (unusual condition)
- From Evolution Capital's paper "Volatility: A New Return Driver?"

---

## Strategy 15: Evolution Capital XIV-Only Strategy

### Rules

**Long XIV when ALL three conditions met:**
1. VIX index closes below front month VIX futures (VIX < VX1)
2. Front month closes below second month (VX1 < VX2)
3. Current roll yield > 20-day average roll yield (RY > 20-day RY)

**Cash when:**
- Any condition not met

### Inputs Required
- VIX spot
- VX1 (front month futures)
- VX2 (second month futures)
- Roll yield and 20-day average

### Traded Instruments
- **XIV** (Short Vol) - only when all conditions align
- **Cash** - otherwise (no VXX position)

### Performance
- Chart shows consistent outperformance vs Buy & Hold XIV
- Smoother equity curve than buy-and-hold

### Notes
- Simplified version of full Evolution Capital strategy
- No long VXX position, only XIV or cash
- All three conditions must be true simultaneously

---

## Strategy 16: DDN's VRP Strategy (Original Formula)

### Rules
- Calculate: 5-day average of [VIX index - (10-day annualized standard deviation of SPY × 100)]
- **Long XIV** when result > threshold (not specified, likely 0)
- **Long VXX** when result ≤ threshold
- Hold until change in position

### Inputs Required
- VIX spot price
- SPY 10-day annualized standard deviation
- 5-day simple moving average

### Traded Instruments
- **XIV** (Short Vol) - when VRP positive
- **VXX** (Long Vol) - when VRP negative

### Performance
- Chart shows growth from $10,000 to over $5,000,000
- Period: 07/2004 to present
- Strong outperformance vs Buy & Hold XIV

### Notes
- Uses 10-day ANNUALIZED standard deviation (different from other versions)
- As originally tested by DDN
- Very strong absolute returns

---

## Strategy 17: VIX Standard Deviation Strategy

### Rules
- **Long VXX** when 10-day standard deviation of daily % changes in VIX index rises above 11%
- Hold VXX until 10-day standard deviation falls below 10%
- **Invest in XIV** when not invested in VXX

### Inputs Required
- VIX daily % changes
- 10-day standard deviation of VIX % changes

### Traded Instruments
- **VXX** (Long Vol) - when VIX volatility high (>11%)
- **XIV** (Short Vol) - when VIX volatility normal (≤10%)

### Performance
- Chart shows exponential growth to over $10,000,000 from $10,000
- Logarithmic scale chart
- Period: mid-2004 to present

### Notes
- Measures volatility OF volatility (VIX's own standard deviation)
- Uses hysteresis: 11% to enter VXX, 10% to exit (avoids whipsaws)
- Transaction costs: 0.1% per trade (0.2% round-trip)
- Return on cash ignored
- Data simulated back to 2004

---

## Strategy 18: The Alpha Strategy (Multi-Rule System)

### Rules

**Rule 1 (High VIX Volatility - Overrides all):**
- Long VXX when standard deviation of VIX over past 10 days > 11%
- Stay in VXX till standard deviation < 10%

**Rule 2 (High Front Month Premium):**
- Long VXX when average front month premium over past 20 days > 5%
- (Only if Rule 1 not active)

**Rule 3 (Neutral Zone):**
- Hold cash if average front month premium over past 20 days between -5% and +5%
- (Only if Rule 1 not active)

**Rule 4 (Low Front Month Premium):**
- Long XIV when average front month premium over past 20 days < -5%
- (Only if Rule 1 not active)

### Inputs Required
- VIX 10-day standard deviation
- Front month VIX futures premium
- 20-day average of front month premium

### Traded Instruments
- **XIV** (Short Vol) - 52% of time
- **VXX** (Long Vol) - 13% of time
- **Cash** - 36% of time

### Performance (2004-2011)
- **Total Return:** 23,661%
- **Annualized Return:** 98%
- **Max Drawdown:** -36%
- **Allocation Changes:** 63
- **Transactions:** 69

**Annual Returns:**
- 2004: 137%
- 2005: 61%
- 2006: 136%
- 2007: 12%
- 2008: 126%
- 2009: 54%
- 2010: 304%
- 2011: 66%

### Notes
- Combines volatility-of-volatility (Rule 1) with term structure (Rules 2-4)
- Rule 1 is highest priority (overrides others)
- Best risk-adjusted returns among 3 models tested
- More robust for varying market conditions vs simpler models

---

## Strategy 19: StDev Model (Rule 1 Only)

### Rules
- Long VXX when standard deviation of VIX over past 10 days > 11%
- Stay in VXX till standard deviation < 10%
- Long XIV when not in VXX

### Inputs Required
- VIX daily % changes
- 10-day standard deviation

### Traded Instruments
- **XIV** (Short Vol) - 89% of time
- **VXX** (Long Vol) - 11% of time
- **Cash** - 0% of time

### Performance (2004-2011)
- **Total Return:** 40,931%
- **Annualized Return:** 112%
- **Max Drawdown:** -59%
- **Allocation Changes:** 31
- **Transactions:** 62

**Annual Returns:**
- 2004: 186%
- 2005: 119%
- 2006: 151%
- 2007: -6%
- 2008: 212%
- 2009: 59%
- 2010: 389%
- 2011: 23%

### Notes
- Highest returns but highest drawdown
- Always fully invested (no cash position)
- 89% of time short volatility
- Less robust than Alpha model
- 2010 exceptional year: 389% return

---

## Strategy 20: Spread Model (Rules 2-4 Only)

### Rules
- Long VXX when average front month premium over past 20 days > 5%
- Hold cash if average front month premium between -5% and +5%
- Long XIV when average front month premium < -5%

### Inputs Required
- Front month VIX futures premium
- 20-day average of front month premium

### Traded Instruments
- **XIV** (Short Vol) - 53% of time
- **VXX** (Long Vol) - 5% of time
- **Cash** - 42% of time

### Performance (2004-2011)
- **Total Return:** 6,643%
- **Annualized Return:** 69%
- **Max Drawdown:** -53%
- **Allocation Changes:** 39
- **Transactions:** 39

**Annual Returns:**
- 2004: 137%
- 2005: 63%
- 2006: 99%
- 2007: -12%
- 2008: 80%
- 2009: 79%
- 2010: 105%
- 2011: 51%

### Notes
- Lowest returns of 3 models
- Most time in cash (42%)
- Only 5% of time long VIX
- More conservative approach
- Moderate drawdown (-53%)

---

# SUMMARY COMPARISON TABLE

## Top Performing Strategies by Annualized Return

| Strategy | Ann. Return | Max DD | Sharpe | Days in Market |
|----------|-------------|--------|--------|----------------|
| StDev Model | 112% | -59% | N/A | 100% |
| Brute Force VRP | 105% | -52.1% | 1.93 | 100% |
| New SVXY Strategy | ~100% | -85%+ | N/A | 100% |
| Alpha Strategy | 98% | -36% | N/A | 64% |
| TTO's Strategy | 83.0% | -65.2% | 1.62 | 100% |
| Macro Investor | 78.2% | -80.1% | 1.34 | 100% |
| Spread Model | 69% | -53% | N/A | 58% |
| QuantStrat TradeR | 64.0% | -32.5% | 1.89 | 64.8% |
| Evolution Capital | 44.3% | -74.9% | 0.94 | 100% |

## Key Insights Across All Strategies

### Common Themes:
1. **All use term structure** - comparing VIX to futures, futures to each other, or VIX to VXV
2. **Smoothing is critical** - use moving averages (5-day, 10-day, 20-day) to avoid whipsaws
3. **Thresholds matter** - 0, 1, 1.25 thresholds dramatically affect performance
4. **Most are binary** - either long XIV or long VXX, few use fractional positions
5. **Cash helps risk management** - strategies using cash positions show better drawdowns

### Risk-Return Tradeoffs:
- **Highest returns** = Highest drawdowns (StDev: 112% return, -59% DD)
- **Best risk-adjusted** = Multi-rule systems (Alpha: 98% return, -36% DD)
- **Most robust** = Cash + multiple signals (Evolution Capital: negative S&P correlation)

### Trading Frequency:
- **Lowest:** 7.4 trades/year (Brute Force VRP)
- **Moderate:** 22-39 trades/year (most strategies)
- **Highest:** 53-69 trades/year (QuantStrat, Alpha)

### Correlation Patterns:
- Most strategies: 10-30% positive correlation to S&P 500
- Buy & Hold XIV: 75-76% positive correlation
- Evolution Capital: **-16.3% negative correlation** (UNIQUE)

### Critical Success Factors:
1. **Concept > Parameters** - underlying edge more important than optimization
2. **Avoid overfitting** - especially with leveraged products or rare conditions
3. **Responsiveness vs stability** - shorter lookbacks more responsive but need wider thresholds
4. **Multiple signals** - combining volatility-of-volatility + term structure improves robustness
5. **Cash management** - reduces drawdowns significantly

