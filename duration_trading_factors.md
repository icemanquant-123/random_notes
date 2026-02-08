# Systematic Duration Trading: Macroeconomic Indicators & Predictive Factors
## A Comprehensive Guide for US Treasury Futures (2Y, 5Y, 10Y, 30Y)

---

## Table of Contents
1. Core Inflation & Growth Indicators (Highest Academic Support)
2. Federal Reserve Policy & Expectations
3. Credit & Risk Premium Indicators
4. Liquidity & Flow Indicators
5. Market-Based Expectations
6. Global Macro Factors
7. Technical & Positioning Indicators
8. Factor Models & Academic Frameworks
9. Trading Strategy Frameworks
10. Data Sources & Implementation

---

## 1. CORE INFLATION & GROWTH INDICATORS
### (Strongest Academic Evidence for Duration Prediction)

### A. Inflation Indicators (Primary Drivers)

#### **1.1 Core PCE (Personal Consumption Expenditures) Deflator**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** Monthly
- **Source:** Bureau of Economic Analysis
- **Why It Matters:** Fed's preferred inflation gauge
- **Trading Signal:**
  - Rising Core PCE → Shorter duration (rates rise)
  - Falling Core PCE → Longer duration (rates fall)
- **Academic Evidence:** Ang & Piazzesi (2003), Ludvigson & Ng (2009)
- **Predictive Power:** 6-12 month horizon
- **Key Thresholds:** Fed targets 2% annually
- **Implementation:** Use YoY change, MoM change, and 3M/6M moving averages

#### **1.2 CPI & Core CPI (Consumer Price Index)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** Monthly
- **Source:** Bureau of Labor Statistics
- **Components to Track:**
  - Core CPI (ex food & energy) - most important
  - Shelter/Rent inflation (sticky component)
  - Services inflation (wage-driven)
  - Supercore CPI (services ex shelter) - Fed focus since 2022
- **Trading Signal:**
  - Upside surprise → Sell duration (especially front end 2Y/5Y)
  - Downside surprise → Buy duration
- **Academic Evidence:** Stock & Watson (1999), Fama & French (1989)
- **Key Derivatives:**
  - 3M/6M/12M momentum
  - YoY vs 3M annualized (trend acceleration/deceleration)
  - Surprise vs consensus

#### **1.3 PPI (Producer Price Index)**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Monthly
- **Leading Indicator:** CPI typically follows PPI with 3-6 month lag
- **Trading Signal:**
  - Rising PPI → Leading indicator of CPI pressure → Sell duration
  - Falling PPI → Disinflation coming → Buy duration
- **Academic Evidence:** Clark (1995)
- **Components:**
  - Core PPI (ex food/energy)
  - PPI for Services
  - PPI for Final Demand

#### **1.4 Import/Export Price Indices**
- **Academic Support:** ⭐⭐⭐
- **Frequency:** Monthly
- **Why It Matters:** Captures global inflation transmission
- **Trading Signal:**
  - Rising import prices → Inflationary pressure → Sell duration
  - Strong dollar + falling import prices → Buy duration

#### **1.5 Inflation Expectations Measures**

**1.5a University of Michigan Inflation Expectations**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** Bi-monthly (preliminary, then final)
- **Horizons:** 1-year, 5-year ahead
- **Why Critical:** Fed watches closely for de-anchoring
- **Trading Signal:**
  - Expectations rising above 3% (1Y) or above 2.5% (5Y) → Major sell duration signal
  - Expectations anchored near 2-2.5% → Neutral
- **Academic Evidence:** Coibion & Gorodnichenko (2015)

**1.5b Survey of Professional Forecasters (SPF)**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Quarterly
- **Source:** Philadelphia Fed
- **Advantage:** Professional forecasters, more stable than consumer surveys

**1.5c New York Fed Survey of Consumer Expectations**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Monthly
- **Advantage:** More granular than Michigan survey

---

### B. Growth Indicators

#### **1.6 Real GDP Growth**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** Quarterly (advance, preliminary, final)
- **Trading Signal:**
  - Strong GDP (>3% annualized) → Sell duration (Fed may tighten)
  - Weak GDP (<1.5% annualized) → Buy duration (Fed may ease)
- **Academic Evidence:** Estrella & Hardouvelis (1991), Harvey (1988)
- **Key Components to Track:**
  - Consumer spending (70% of GDP)
  - Business investment
  - Net exports
  - Government spending
- **High-Frequency Proxies:**
  - GDPNow (Atlanta Fed) - real-time GDP estimate
  - Blue Chip consensus
  - Nowcasting models

#### **1.7 Employment Data**

**1.7a Nonfarm Payrolls (NFP)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** Monthly (first Friday)
- **Trading Signal:**
  - Strong jobs (>250K, unemployment falling) → Sell duration
  - Weak jobs (<150K, unemployment rising) → Buy duration
- **Academic Evidence:** Andersen et al. (2007)
- **Components:**
  - Headline payrolls
  - Unemployment rate
  - Labor force participation
  - Average hourly earnings (wage inflation)
  - Average weekly hours
- **Key Thresholds:**
  - Unemployment <4% = tight labor market = inflation risk
  - Unemployment >5% = slack = disinflation

**1.7b JOLTS (Job Openings and Labor Turnover Survey)**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Monthly (with lag)
- **Components:**
  - Job openings (demand)
  - Quits (worker confidence)
  - Hires (matching efficiency)
  - Layoffs (stress indicator)
- **Trading Signal:**
  - Job openings/unemployed ratio >1.5 → Tight labor market → Sell duration
  - Ratio <1.0 → Slack → Buy duration

**1.7c Initial & Continuing Jobless Claims**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Weekly
- **Advantage:** Highest frequency macro data
- **Trading Signal:**
  - Claims <200K → Strong labor market → Sell duration
  - Claims >300K and rising → Weakening → Buy duration
  - 4-week moving average crossing above/below trend
- **Leading Indicator:** Claims typically lead payrolls by 1-2 months

**1.7d ADP Employment Report**
- **Academic Support:** ⭐⭐⭐
- **Frequency:** Monthly (2 days before NFP)
- **Use:** Leading indicator for NFP, though imperfect correlation

#### **1.8 ISM Manufacturing & Services PMI**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** Monthly (first business day)
- **Trading Signal:**
  - PMI >55 → Strong expansion → Sell duration
  - PMI 50-55 → Moderate growth → Neutral
  - PMI 45-50 → Contraction territory → Buy duration
  - PMI <45 → Deep contraction → Strong buy duration
- **Academic Evidence:** Lahiri & Moore (1991)
- **Key Components:**
  - New Orders (leading indicator)
  - Prices Paid (inflation gauge)
  - Employment
  - Inventories (cycle position)
- **Services PMI:** More important (80% of economy) but less market-moving historically

#### **1.9 Retail Sales**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Monthly (mid-month)
- **Trading Signal:**
  - Strong growth (>0.5% MoM) → Economic strength → Sell duration
  - Weak/negative → Economic weakness → Buy duration
- **Key Metrics:**
  - Headline retail sales
  - Retail sales ex autos
  - Retail sales ex autos & gas (control group)

#### **1.10 Industrial Production & Capacity Utilization**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Monthly (mid-month)
- **Trading Signal:**
  - Capacity utilization >80% → Inflationary pressure → Sell duration
  - Capacity utilization <75% → Slack → Buy duration
- **Academic Evidence:** Garner (1995)

#### **1.11 Consumer & Business Confidence**
- **Academic Support:** ⭐⭐⭐
- **Conference Board Consumer Confidence:** Monthly
- **University of Michigan Consumer Sentiment:** Bi-monthly
- **CEO Confidence Survey:** Quarterly
- **Trading Signal:**
  - Rising confidence → Future growth strength → Sell duration
  - Falling confidence → Economic weakness ahead → Buy duration

---

## 2. FEDERAL RESERVE POLICY & EXPECTATIONS

### A. Fed Funds Rate & Policy

#### **2.1 Federal Funds Target Rate**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Why It Matters:** Direct control of short-term rates
- **Trading Signal:**
  - Expected hikes → Sell front-end duration (2Y/5Y more than 10Y/30Y)
  - Expected cuts → Buy front-end duration
  - Terminal rate expectations drive entire curve
- **Academic Evidence:** Bernanke & Kuttner (2005), Gürkaynak et al. (2005)

#### **2.2 Fed Dot Plot**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** Quarterly (with SEP - Summary of Economic Projections)
- **Why Critical:** Forward guidance on rate path
- **Trading Signal:**
  - Median dot above market pricing → Sell duration
  - Median dot below market pricing → Buy duration
  - Dispersion in dots → Uncertainty → Higher term premium
- **Key Metrics:**
  - Current year median
  - Next year median
  - Longer-run median (neutral rate estimate)
  - Number of dots expecting cuts vs hikes

#### **2.3 FOMC Statements & Minutes**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Frequency:** 8 meetings/year, minutes 3 weeks after
- **Why Critical:** Policy stance, forward guidance, reaction function
- **Key Language Changes:**
  - "Considerable time" → "Patient" → "Data-dependent"
  - Risk balance: "Two-sided risks" vs "Upside risks to inflation"
  - Employment language: "Maximum employment" vs "Labor market remains tight"
- **Trading Implementation:**
  - Text analysis for hawkish/dovish shift
  - Compare vs previous statement
  - Fed speak decoder (e.g., "significant" vs "material" vs "modest")

#### **2.4 Fed Chair Speeches & Testimony**
- **Academic Support:** ⭐⭐⭐⭐
- **Jackson Hole Symposium:** August, major policy signals
- **Semi-Annual Testimony:** February & July to Congress
- **Other Speeches:** Watch for policy-relevant content
- **Trading Signal:** Real-time reaction to hawkish/dovish tone

#### **2.5 Fed Balance Sheet & QE/QT**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Metrics:**
  - Total assets (FRED: WALCL)
  - Treasury holdings
  - MBS holdings
  - Pace of QT (caps on runoff)
- **Trading Signal:**
  - QE (balance sheet expansion) → Buy duration (lower term premium)
  - QT (balance sheet reduction) → Sell duration (higher term premium)
- **Academic Evidence:** Gagnon et al. (2011), Krishnamurthy & Vissing-Jorgensen (2011)
- **Key Research:** Each $100B in QE ≈ 3-5bps compression in 10Y

---

### B. Market-Based Fed Expectations

#### **2.6 Fed Funds Futures**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Why Critical:** Real-time market pricing of Fed path
- **Trading Signal:**
  - Compare implied Fed path vs dots/guidance
  - Implied rate > current → Sell duration
  - Implied rate < current → Buy duration
- **Key Metrics:**
  - Implied rate for next meeting
  - Probability of cut/hike/hold
  - Terminal rate pricing
  - Timing of first cut/hike
- **Tools:** CME FedWatch Tool

#### **2.7 Overnight Index Swaps (OIS)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Why Better Than Futures:** Pure rate expectation, no convexity
- **Key Tenors:** 1M, 3M, 6M, 1Y, 2Y, 5Y, 10Y
- **Trading Signal:**
  - OIS curve steepening → Expectations of hikes → Sell duration
  - OIS curve flattening/inverting → Expectations of cuts → Buy duration

#### **2.8 SOFR (Secured Overnight Financing Rate)**
- **Academic Support:** ⭐⭐⭐⭐
- **Replacement for LIBOR (2023+)
- **Why It Matters:** Basis for short-term rate expectations
- **Trading Implementation:**
  - Monitor SOFR vs Fed Funds spread
  - SOFR futures curve shape

---

## 3. CREDIT & RISK PREMIUM INDICATORS

### A. Credit Spreads

#### **3.1 Investment Grade (IG) Corporate Spreads**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Metrics:**
  - OAS (Option-Adjusted Spread) to Treasuries
  - BBB spreads (lowest IG tier)
  - A-rated spreads
- **Trading Signal:**
  - Widening spreads (>150bps for IG) → Risk-off → Buy duration (flight to quality)
  - Tightening spreads (<100bps) → Risk-on → Sell duration
- **Academic Evidence:** Longstaff et al. (2005), Gilchrist & Zakrajšek (2012)
- **Key Research:** GZ spread (Gilchrist-Zakrajšek excess bond premium) predicts economic activity

#### **3.2 High Yield (HY) Spreads**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Metrics:**
  - OAS to worst
  - Distress ratio (% yielding >1000bps)
  - Default rate expectations
- **Trading Signal:**
  - HY spreads >500bps → Financial stress → Buy duration
  - HY spreads <300bps → Complacency → Risk of reversal
- **Academic Evidence:** Collin-Dufresne et al. (2001)

#### **3.3 Credit Default Swaps (CDS)**
- **Academic Support:** ⭐⭐⭐⭐
- **Key Indices:**
  - CDX IG (investment grade)
  - CDX HY (high yield)
  - iTraxx (European)
- **Advantage:** More liquid and forward-looking than cash bonds
- **Trading Signal:** Similar to cash spreads

---

### B. Equity Market Risk Indicators

#### **3.4 VIX (Volatility Index)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Why It Matters:** "Fear gauge" - risk appetite
- **Trading Signal:**
  - VIX >25 → Risk-off → Buy duration (flight to quality)
  - VIX <15 → Complacency → Neutral/sell duration
  - VIX spike >10 points intraday → Immediate buy duration
- **Academic Evidence:** Whaley (2000), Bekaert & Hoerova (2014)
- **Related Metrics:**
  - VIX futures term structure (contango vs backwardation)
  - MOVE index (bond market volatility)

#### **3.5 Equity Put/Call Ratio**
- **Academic Support:** ⭐⭐⭐
- **Trading Signal:**
  - High put/call ratio (>1.0) → Fear → Buy duration
  - Low put/call ratio (<0.7) → Complacency

#### **3.6 Equity Market Performance**
- **Academic Support:** ⭐⭐⭐⭐
- **S&P 500 vs Treasuries:**
  - Stock market crash → Buy duration (flight to quality)
  - Strong equity rally → Sell duration (risk-on, growth expectations)
- **Academic Evidence:** Campbell & Ammer (1993)
- **Key Metrics:**
  - 1M/3M/6M equity returns
  - Equity drawdowns (peak-to-trough)
  - Stock-bond correlation regime

---

## 4. LIQUIDITY & FLOW INDICATORS

#### **4.1 Treasury Auction Results**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Weekly (bills), monthly (notes/bonds)
- **Key Metrics:**
  - Bid-to-Cover ratio (demand strength)
  - Indirect bidder % (foreign demand)
  - Direct bidder % (domestic non-dealer)
  - Primary dealer takedown
  - Tail (high yield vs when-issued)
- **Trading Signal:**
  - Strong auction (high B/C, low tail) → Buy duration
  - Weak auction (low B/C, large tail) → Sell duration
- **Academic Evidence:** Lou et al. (2013)

#### **4.2 Foreign Central Bank Holdings (TIC Data)**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Monthly (with 6-week lag)
- **Source:** Treasury International Capital (TIC) system
- **Trading Signal:**
  - Foreign accumulation → Buy duration (demand support)
  - Foreign selling → Sell duration (reduced demand)
- **Key Players:**
  - China (largest foreign holder)
  - Japan (second largest)
  - Oil exporters (petrodollar recycling)
  - European central banks
- **Academic Evidence:** Warnock & Warnock (2009)

#### **4.3 Repo Market Conditions**
- **Academic Support:** ⭐⭐⭐⭐
- **Key Metrics:**
  - General collateral (GC) repo rate
  - Repo-OIS spread
  - SOFR-IOER spread
  - Repo fails (settlement fails indicate scarcity)
- **Trading Signal:**
  - Repo rate spikes → Funding stress → Buy duration
  - Negative repo-OIS spread → Excess liquidity → Sell duration
- **Academic Evidence:** Gorton & Metrick (2012)

#### **4.4 Reserve Balances at Fed**
- **Academic Support:** ⭐⭐⭐⭐
- **Source:** FRED (RESBALNS)
- **Trading Signal:**
  - Declining reserves below $2.5T → Liquidity concerns → Higher term premium
  - Ample reserves → Smooth functioning → Lower term premium

#### **4.5 Primary Dealer Positioning**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Source:** NY Fed weekly
- **Key Metrics:**
  - Net positioning (long vs short)
  - Inventory levels by tenor
  - Fails to deliver/receive
- **Trading Signal:**
  - Dealers net short → Potential short squeeze → Buy duration
  - Dealers overleveraged long → Potential forced selling → Sell duration
- **Academic Evidence:** Adrian et al. (2014)

#### **4.6 CFTC Positioning (Commitment of Traders)**
- **Academic Support:** ⭐⭐⭐⭐
- **Frequency:** Weekly
- **Categories:**
  - Asset Manager/Institutional
  - Leveraged Funds (hedge funds)
  - Dealer/Intermediary
- **Trading Signal:**
  - Extreme positioning (>2 std dev) → Reversal risk
  - Leveraged funds extremely long → Sell signal
  - Leveraged funds extremely short → Buy signal
- **Academic Evidence:** Wang (2003)

---

## 5. MARKET-BASED EXPECTATIONS

### A. Yield Curve Metrics

#### **5.1 Yield Curve Slope**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Key Spreads:**
  - 10Y-2Y (most watched recession indicator)
  - 10Y-3M (more leading recession indicator)
  - 30Y-5Y (long-end term premium)
  - 5Y-2Y (belly steepness)
- **Trading Signal:**
  - Inversion (negative slope) → Recession risk → Buy long duration
  - Steepening from inversion → Recovery expectations
  - Bull steepening (front falls more) → Easing cycle → Buy duration
  - Bear steepening (long rises more) → Inflation concerns → Sell long end
  - Bull flattening (long falls more) → Disinflation → Buy long duration
  - Bear flattening (front rises more) → Tightening cycle → Sell front end
- **Academic Evidence:** 
  - Estrella & Mishkin (1998) - inversion predicts recession
  - Ang & Piazzesi (2003) - slope predicts excess bond returns
  - Cochrane & Piazzesi (2005) - forward rates predict returns

#### **5.2 Term Premium Decomposition**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Models:**
  - **ACM Term Premium (Adrian, Crump, Moench)** - NY Fed
  - **Kim-Wright Term Premium** - Fed Board
- **Trading Signal:**
  - Negative term premium → Extremely low long rates → Sell long duration
  - Rising term premium → Compensation increasing → Buy long duration attractive
- **Academic Evidence:** Adrian et al. (2013), Kim & Wright (2005)
- **Why It Matters:** Separates rate expectations from risk premium

#### **5.3 Breakeven Inflation Rates (TIPS spread)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Calculation:** Nominal yield - TIPS yield
- **Key Tenors:** 5Y, 10Y, 30Y breakevens
- **Trading Signal:**
  - Breakevens rising above Fed target (>2.5%) → Inflation expectations unanchoring → Sell nominals
  - Breakevens falling below 1.5% → Deflation fears → Buy nominals (relative to TIPS)
- **Derived Metrics:**
  - 5Y5Y forward breakeven (5Y inflation 5 years forward) - Fed watches this
  - 10Y breakeven vs realized CPI (over/under-pricing)
- **Academic Evidence:** Gürkaynak et al. (2007)

#### **5.4 Real Yields (TIPS)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Trading Signal:**
  - Negative real yields → Accommodative policy → Economy needs support
  - Positive real yields >1% → Restrictive policy → Slowing growth
  - Rising real yields → Sell nominals, buy TIPS
  - Falling real yields → Buy nominals
- **Academic Evidence:** Campbell & Shiller (1991)

---

### B. Forward Rates & Curve Models

#### **5.5 Forward Rate Curve**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Key Forwards:**
  - 1Y1Y (1-year rate, 1 year forward)
  - 2Y1Y, 5Y5Y, 5Y10Y
- **Trading Signal:**
  - Forward curve inversion → Future easing priced → Buy duration
  - Forward curve steep → Future tightening → Sell duration
- **Academic Evidence:** Fama & Bliss (1987), Cochrane & Piazzesi (2005)

#### **5.6 Principal Component Analysis (PCA)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **First 3 PCs explain ~99% of yield curve variation:**
  - **PC1 (Level):** ~90% - parallel shifts
  - **PC2 (Slope):** ~7% - steepening/flattening  
  - **PC3 (Curvature):** ~2% - butterfly
- **Trading Implementation:**
  - Monitor PC factor loadings
  - Trade deviations from historical relationships
- **Academic Evidence:** Litterman & Scheinkman (1991)

---

## 6. GLOBAL MACRO FACTORS

#### **6.1 US Dollar (DXY Index)**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Trading Signal:**
  - Strong dollar → Imported disinflation → Buy duration
  - Weak dollar → Imported inflation → Sell duration
  - Dollar inversely related to commodities
- **Academic Evidence:** Clarida & Gali (1994)
- **Key Currency Pairs:**
  - EUR/USD (57% of DXY)
  - USD/JPY (13% of DXY)
  - GBP/USD (12% of DXY)

#### **6.2 Foreign Interest Rates**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Key Rates:**
  - German Bund (10Y) - European benchmark
  - UK Gilt (10Y)
  - Japanese JGB (10Y)
  - Canadian Government Bonds
- **Trading Signal:**
  - Foreign yields rising faster → US rates follow → Sell duration
  - Foreign yields negative/very low → Buy US duration on relative value
- **Academic Evidence:** Ehrmann et al. (2011) - spillovers
- **Key Spreads:**
  - UST 10Y - Bund 10Y (typical range: 150-250bps)
  - Widening spread → Dollar strength, US growth premium

#### **6.3 Commodity Prices**
- **Academic Support:** ⭐⭐⭐⭐
- **Key Commodities:**
  - **Crude Oil (WTI, Brent)** - inflation pass-through
  - **Gold** - inflation hedge, monetary policy expectations
  - **Copper** - "Dr. Copper" growth indicator
  - **Agricultural** - food price inflation
- **Trading Signal:**
  - Oil >$90/bbl → Inflation pressure → Sell duration
  - Oil <$60/bbl → Disinflationary → Buy duration
  - Gold rallying with real yields falling → Monetary easing → Buy duration
  - Copper surging → Global growth → Sell duration
- **Academic Evidence:** Barsky & Kilian (2004)

#### **6.4 Global PMIs**
- **Academic Support:** ⭐⭐⭐⭐
- **Key Regions:**
  - Eurozone PMI (Composite, Manufacturing, Services)
  - China Caixin PMI
  - UK PMI
  - Japan PMI
- **Trading Signal:**
  - Global growth acceleration → Sell UST duration
  - Global slowdown → Buy UST duration (safe haven)

#### **6.5 Emerging Market Indicators**
- **Academic Support:** ⭐⭐⭐
- **Key Metrics:**
  - EM FX (risk appetite)
  - EM sovereign spreads (EMBI)
  - EM equity performance
- **Trading Signal:**
  - EM stress → Flight to quality → Buy UST duration
  - EM strength → Risk-on → Sell UST duration

---

## 7. TECHNICAL & POSITIONING INDICATORS

#### **7.1 Moving Averages**
- **Academic Support:** ⭐⭐⭐
- **Key MAs:** 50-day, 100-day, 200-day
- **Trading Signal:**
  - Yield crosses above 200-day MA → Sell duration
  - Yield crosses below 200-day MA → Buy duration
  - Golden cross (50 above 200) vs Death cross

#### **7.2 Momentum Indicators**
- **Academic Support:** ⭐⭐⭐⭐
- **RSI (Relative Strength Index)**
  - >70 → Overbought (yields high) → Buy duration
  - <30 → Oversold (yields low) → Sell duration
- **MACD:** Trend following
- **Academic Evidence:** Moskowitz et al. (2012) - time series momentum

#### **7.3 Volume & Liquidity Metrics**
- **Academic Support:** ⭐⭐⭐⭐
- **Metrics:**
  - TRACE volume (corporate bonds)
  - Treasury trading volume
  - Bid-ask spreads
  - Market depth
- **Trading Signal:**
  - Declining liquidity → Higher volatility → Wider trading ranges
  - Volume surges → Confirm trend moves

#### **7.4 Sentiment Indicators**
- **Academic Support:** ⭐⭐⭐
- **Surveys:**
  - Bank of America Fund Manager Survey
  - AAII Sentiment Survey
  - Investors Intelligence Survey
- **Trading Signal:**
  - Extreme bullish sentiment (>60%) → Contrarian sell
  - Extreme bearish sentiment (<30%) → Contrarian buy

---

## 8. FACTOR MODELS & ACADEMIC FRAMEWORKS

### A. Structural Models

#### **8.1 Taylor Rule**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Formula:** r* = neutral rate + inflation + 0.5×(inflation - target) + 0.5×(output gap)
- **Trading Implementation:**
  - Compare Taylor Rule implied rate vs actual Fed Funds
  - If Taylor > Fed Funds → Fed behind curve → Sell duration
  - If Taylor < Fed Funds → Fed ahead of curve → Buy duration
- **Academic Evidence:** Taylor (1993), Clarida et al. (2000)
- **Variants:**
  - Balanced approach (equal weights)
  - Inertial (includes lagged rate)
  - Mankiw rule (different weights)

#### **8.2 Yield Curve Arbitrage Models**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Approaches:**
  - Nelson-Siegel model (level, slope, curvature)
  - Diebold-Li dynamic Nelson-Siegel
  - Affine term structure models
- **Trading Implementation:**
  - Identify rich/cheap along curve
  - Mean reversion trades
- **Academic Evidence:** Nelson & Siegel (1987), Diebold & Li (2006)

---

### B. Return Prediction Models

#### **8.3 Cochrane-Piazzesi Factor**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **What It Is:** Linear combination of forward rates predicts excess bond returns
- **Trading Implementation:**
  - High CP factor → High expected returns → Buy duration
  - Low CP factor → Low expected returns → Sell duration
- **Academic Evidence:** Cochrane & Piazzesi (2005)
- **Predictive Horizon:** 1-year forward returns
- **R-squared:** ~30% for 1Y ahead excess returns

#### **8.4 Ludvigson-Ng Macro Factors**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **What It Is:** Principal components from 132 macro time series
- **Factors:**
  - Real activity factor
  - Inflation factor  
  - Financial/monetary policy factor
- **Trading Implementation:**
  - Rising real activity factor → Sell duration
  - Rising inflation factor → Sell duration
  - Easing monetary factor → Buy duration
- **Academic Evidence:** Ludvigson & Ng (2009)

#### **8.5 Carry Trade**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **Strategy:** Buy high-yielding duration, sell low-yielding
- **Implementation:**
  - Long 30Y, short 2Y (when positively sloped)
  - Roll down the curve
- **Academic Evidence:** Ang et al. (2006)
- **Risk:** Curve inversion, parallel shifts

---

### C. Regime-Based Models

#### **8.6 Business Cycle Indicators**
- **Academic Support:** ⭐⭐⭐⭐⭐
- **NBER Recession Indicators:**
  - Leading Economic Index (LEI)
  - Coincident Economic Index (CEI)
  - Lagging Economic Index
- **Trading Signal:**
  - LEI declining 6+ months → Recession risk → Buy duration
  - LEI rising → Expansion → Sell duration
- **Academic Evidence:** Stock & Watson (1989)
- **Conference Board LEI Components:**
  - Average weekly hours (manufacturing)
  - Initial jobless claims
  - New orders (consumer goods)
  - ISM new orders
  - Building permits
  - Stock prices
  - Leading Credit Index
  - Interest rate spread (10Y-Fed Funds)
  - Consumer expectations

#### **8.7 Growth-Inflation Regimes**
- **Academic Support:** ⭐⭐⭐⭐
- **Four Quadrants:**
  1. **Goldilocks** (Growth↑, Inflation↓) → Sell duration (risk-on)
  2. **Reflation** (Growth↑, Inflation↑) → Sell duration (Fed tightening risk)
  3. **Stagflation** (Growth↓, Inflation↑) → Complex (short end falls, long rises)
  4. **Deflation** (Growth↓, Inflation↓) → Buy duration (easing cycle)
- **Academic Evidence:** Blitz & Van Vliet (2008)

---

## 9. TRADING STRATEGY FRAMEWORKS

### A. Directional Strategies

#### **9.1 Macro Trend Following**
- **Approach:** Combine macro factors into hawkish/dovish score
- **Example Scorecard:**
  - Inflation (CPI, PCE, PPI) → Weight 30%
  - Growth (GDP, employment, PMI) → Weight 25%
  - Fed policy (dots, statements, futures) → Weight 25%
  - Risk sentiment (VIX, credit spreads) → Weight 10%
  - Global factors (DXY, foreign rates) → Weight 10%
- **Signal Generation:**
  - Aggregate score >+2 std dev → Sell duration
  - Aggregate score <-2 std dev → Buy duration
- **Position Sizing:** Scale by conviction (distance from neutral)

#### **9.2 Event-Driven Trading**
- **Key Events:**
  - FOMC meetings (8/year)
  - CPI/PCE releases (monthly)
  - NFP (monthly)
  - Treasury auctions (weekly)
  - Fed speeches
  - Debt ceiling debates
  - Fed Chair nomination/confirmation
- **Implementation:**
  - Pre-position based on expectations
  - Trade the surprise component
  - Fade extreme moves if fundamentals haven't changed

---

### B. Relative Value Strategies

#### **9.3 Curve Steepeners/Flatteners**
- **Implementation:**
  - Bull steepener: Long 30Y, short 5Y (Fed easing)
  - Bear steepener: Short 2Y, long 30Y (inflation concerns)
  - Bull flattener: Long 2Y, short 30Y (disinflation)
  - Bear flattener: Short 30Y, long 2Y (Fed hiking)
- **Risk Management:**
  - Duration-neutral (DV01 match)
  - Monitor parallel shift risk
- **Academic Evidence:** Litterman & Scheinkman (1991)

#### **9.4 Butterfly Trades**
- **Structure:** Body (5Y or 10Y) vs wings (2Y+30Y or 5Y+30Y)
- **Trading Signal:**
  - Flattening butterfly (body outperforms) → Economic uncertainty
  - Steepening butterfly (wings outperform) → Clarity on direction
- **Academic Evidence:** Knez et al. (1994)

#### **9.5 Rich/Cheap Analysis**
- **Approaches:**
  - Relative to fitted curve (Nelson-Siegel)
  - Relative to historical spread
  - Relative to duration-matched corporates
- **Implementation:**
  - Buy cheap tenor, sell rich tenor
  - Mean reversion assumption

---

### C. Hedging Strategies

#### **9.6 Convexity Hedging**
- **What:** Gamma hedging for mortgage portfolios
- **Impact on Treasuries:**
  - Rates falling → Prepayments up → Hedgers sell duration → Rates rise more
  - Rates rising → Hedgers buy duration → Dampens rate rise
- **Trading Signal:**
  - Large mortgage hedging flow → Exacerbates moves
  - Monitor MBS duration, rate of change

#### **9.7 Tail Risk Hedging**
- **Instruments:**
  - Long OTM puts on TLT/IEF
  - Long VIX calls
  - Long Treasury futures in risk-off scenarios
- **When to Use:**
  - Elevated VIX
  - Recession risks
  - Financial system stress

---

## 10. DATA SOURCES & IMPLEMENTATION

### A. Free Data Sources

#### **10.1 Government Sources**
- **FRED (St. Louis Fed):** Comprehensive macro database
  - All major indicators
  - API available
  - Historical data
- **BEA (Bureau of Economic Analysis):** GDP, PCE
- **BLS (Bureau of Labor Statistics):** CPI, employment
- **Treasury Direct:** Auction results
- **NY Fed:** Primary dealer data, SOFR, term premiums
- **Philadelphia Fed:** SPF, state coincident indices
- **Atlanta Fed:** GDPNow, wage tracker
- **Cleveland Fed:** Inflation nowcasting

#### **10.2 Market Data**
- **CME Group:** Futures prices, volume, open interest
- **ICE:** CDS indices
- **FINRA TRACE:** Corporate bond trades
- **SIFMA:** Issuance calendars, trading statistics

---

### B. Premium Data Vendors

#### **10.3 Bloomberg Terminal**
- **Functions:**
  - OMON (Options Monitor)
  - FWCV (Forward Curve)
  - SWPM (Swap Manager)
  - BTMM (Bond Trade Match)
  - CMBQ (CFTC positioning)
  - WIRP (Fed pricing)
- **Advantages:** Real-time, comprehensive, analytics

#### **10.4 Refinitiv (formerly Thomson Reuters)**
- **Eikon platform**
- **Datastream for historical**

#### **10.5 FactSet**
- **Strong on fundamentals**
- **Good API**

---

### C. Academic & Research Sources

#### **10.6 Key Research Repositories**
- **NBER Working Papers**
- **SSRN**
- **Fed working papers (Board, regional banks)**
- **BIS working papers**
- **ECB working papers**

#### **10.7 Key Journals**
- **Journal of Finance**
- **Journal of Financial Economics**
- **Review of Financial Studies**
- **Journal of Monetary Economics**
- **American Economic Review**

---

## RECOMMENDED FACTOR HIERARCHY FOR SYSTEMATIC TRADING

### Tier 1: Core Macro (70% weight)
1. **Inflation** (30%): Core PCE, CPI, PPI, inflation expectations
2. **Fed Policy** (25%): Dots, FOMC, Fed Funds futures, OIS
3. **Growth** (15%): GDP, employment, PMIs

### Tier 2: Market Expectations (20% weight)
4. **Yield Curve** (10%): Slope, term premium, forward rates
5. **Credit/Risk** (10%): IG/HY spreads, VIX

### Tier 3: Technical/Positioning (10% weight)
6. **Flows** (5%): CFTC, dealers, auctions
7. **Momentum/Technicals** (5%): Moving averages, RSI

---

## SYSTEMATIC IMPLEMENTATION FRAMEWORK

### Step 1: Data Collection
- Automate data pulls (APIs, web scraping)
- Store in time-series database
- Handle revisions, lags, different frequencies

### Step 2: Signal Generation
- Normalize all indicators (z-scores)
- Weight by academic evidence + backtested predictive power
- Combine into master signal (-100 to +100)

### Step 3: Position Construction
- Map signal to position: -100 = max short, +100 = max long
- Determine which tenor(s) to trade based on:
  - 2Y: Most Fed-sensitive, front-end trades
  - 5Y: Belly, balanced exposure
  - 10Y: Benchmark, most liquid
  - 30Y: Term premium, inflation expectations
- Consider curve trades (steepeners/flatteners)

### Step 4: Risk Management
- Maximum position size limits
- Stop losses (technical + fundamental)
- Rebalance frequency (daily, weekly, monthly)
- Drawdown limits

### Step 5: Execution
- Futures vs cash (futures more liquid)
- Time of day (on-the-run trading)
- Minimize market impact
- Use limit orders when possible

### Step 6: Performance Monitoring
- Track P&L by factor
- Attribution analysis
- Correlation to benchmarks
- Sharpe ratio, max drawdown
- Factor decay analysis

---

## ACADEMIC EVIDENCE SUMMARY

### Most Robust Predictors (Sharpe >0.5 in academic studies):
1. **Yield curve slope** (10Y-2Y, 10Y-3M)
2. **Cochrane-Piazzesi factor**
3. **Forward rate factor**
4. **Fed policy surprises**
5. **Term premium**
6. **Credit spreads** (GZ spread)
7. **Inflation surprises**
8. **Employment data**
9. **Foreign interest rates**
10. **Macro factors** (Ludvigson-Ng)

### Timeframe Consistency:
- **Short-term (<1 month):** Fed policy, data surprises, technical
- **Medium-term (1-6 months):** Growth, inflation, credit conditions
- **Long-term (6+ months):** Cycle position, term premium, structural factors

---

## KEY RESEARCH PAPERS (Essential Reading)

1. **Cochrane, J. H., & Piazzesi, M. (2005).** "Bond Risk Premia." American Economic Review.
   - **Finding:** Forward rates predict excess bond returns

2. **Ludvigson, S. C., & Ng, S. (2009).** "Macro Factors in Bond Risk Premia." Review of Financial Studies.
   - **Finding:** Real activity and inflation factors predict returns

3. **Ang, A., & Piazzesi, M. (2003).** "A No-Arbitrage Vector Autoregression of Term Structure Dynamics." Journal of Monetary Economics.
   - **Finding:** Macro factors price bonds

4. **Estrella, A., & Mishkin, F. S. (1998).** "Predicting US Recessions." Review of Economics and Statistics.
   - **Finding:** Yield curve slope predicts recessions 6-18 months ahead

5. **Adrian, T., Crump, R. K., & Moench, E. (2013).** "Pricing the Term Structure with Linear Regressions." Journal of Financial Economics.
   - **Finding:** Simple regression predicts term premium

6. **Bernanke, B. S., & Kuttner, K. N. (2005).** "What Explains the Stock Market's Reaction to Federal Reserve Policy?" Journal of Finance.
   - **Finding:** Only policy surprises move markets

7. **Gilchrist, S., & Zakrajšek, E. (2012).** "Credit Spreads and Business Cycle Fluctuations." American Economic Review.
   - **Finding:** GZ spread predicts economic activity

8. **Gürkaynak, R. S., Sack, B., & Swanson, E. (2005).** "Do Actions Speak Louder Than Words?" International Journal of Central Banking.
   - **Finding:** Fed communication moves markets

9. **Fama, E. F., & Bliss, R. R. (1987).** "The Information in Long-Maturity Forward Rates." American Economic Review.
   - **Finding:** Forward rates contain information about future spot rates

10. **Krishnamurthy, A., & Vissing-Jorgensen, A. (2011).** "The Effects of Quantitative Easing on Interest Rates." Brookings Papers.
    - **Finding:** QE significantly lowers yields

---

## FINAL RECOMMENDATIONS

### For Institutional/Algorithmic Traders:
1. Build comprehensive macro database (FRED API + vendors)
2. Implement Ludvigson-Ng or similar factor model
3. Layer Cochrane-Piazzesi return prediction
4. Add regime detection (growth/inflation quadrants)
5. Use Kelly criterion for position sizing
6. Backtest rigorously (30+ years if possible)
7. Account for transaction costs, slippage
8. Monitor live performance vs backtest

### For Discretionary Traders:
1. Focus on Tier 1 factors (inflation, Fed, growth)
2. Maintain macro dashboard with z-scores
3. Trade major events (FOMC, CPI, NFP)
4. Use technical for entry/exit timing
5. Size positions by conviction + volatility
6. Keep detailed trade journal
7. Post-mortem every trade

### For Risk Managers:
1. Stress test portfolio across scenarios
2. Monitor factor exposures (DV01, convexity)
3. Set VaR limits
4. Correlation regime monitoring
5. Liquidity buffers

---

## CONCLUSION

Duration trading success requires:
1. **Macro foundation:** Understand inflation, growth, Fed policy
2. **Academic rigor:** Use proven factors, not curve-fit indicators  
3. **Systematic process:** Remove emotion, follow signals
4. **Risk discipline:** Size appropriately, cut losses
5. **Continuous learning:** Markets evolve, models must adapt

The factors outlined above represent the intersection of academic research and practitioner wisdom. Weight them according to your timeframe, risk tolerance, and market regime.

**Most important:** The relationship between macro factors and bond yields can shift. What worked in 2010-2020 (low rates, QE) may not work in 2020s (higher inflation regime). Always validate relationships in current market environment.

