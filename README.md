## Overview
This project analyzes 2026 NBA prospects relative to historical NBA superstar college profiles using a composite scoring framework. By standardizing key impact, efficiency, and usage metrics across a combined dataset of prospects and established NBA superstars, the dashboard evaluates how closely each prospect aligns with elite collegiate archetypes.

Rather than producing deterministic draft predictions, the project emphasizes comparative modeling and archetype-based benchmarking. This was my first end-to-end Tableau modeling dashboard, built to explore composite prospect evaluation using historical performance benchmarks.

## Final Project
<img width="1610" height="801" alt="image" src="https://github.com/user-attachments/assets/882a3f29-e15a-4371-b3b5-1aae0c9669da" />

## Objectives
- Compare 2026 NBA prospects to historical NBA superstar college benchmarks
- Engineer composite indices to measure offensive impact, efficiency, and two-way contribution
- Normalize performance metrics using Z-scores for cross-player comparability
- Identify prospects with strong archetype alignment to elite college profiles
- Create an interactive Tableau dashboard to visualize composite scoring and benchmark comparisons

## Tools
- Tableau (data modeling, calculated fields, dashboard design)
- CSV-based college basketball datasets (prospects + historical NBA superstars)
- Git/GitHub for version control and documentation

## Dataset
Stats were taken from barttorvik.com as of February 5th, 2026. The dataset combines:
- 2026 NBA draft prospects (college statistics)
- Historical NBA superstars and their college performance metrics

Core statistics used in modeling:

- Box Plus/Minus (BPM)
- Points Over Replacement Per Game (PRPG!)
- Assist Contributed to Team Rate (AST%)
- Usage Rate (USG%)
- True Shooting Percentage (TS%)
- Additional supporting efficiency and impact indicators

All metrics were standardized across the full combined dataset to ensure consistent comparability.

## Methodology
- Combined prospect and historical superstar datasets into a unified model
- Standardized all key performance metrics using Z-score normalization
- Engineered multiple composite indices to capture different dimensions of player impact
- Established historical superstar college averages as benchmark reference lines
- Ranked prospects based on composite scores and archetype similarity
- Designed a structured Tableau dashboard to visualize rankings, distributions, and benchmark comparisons

## Composite Scoring Framework
### Superstar Score
A composite score designed to measure how closely a prospect’s college statistical profile aligns with historical NBA superstar benchmarks. This score aggregates standardized impact and usage-based metrics to capture both production and offensive responsibility.
- (0.40 × Offensive Impact) + (0.30 × Efficiency vs Usage) + (0.30 × Two-Way Impact)
### Offensive Index Score
A composite of offensive production and efficiency metrics, emphasizing scoring impact, usage rate, and playmaking indicators.
- (0.30 × Usg%) + (0.25 × TS%) + (0.20 × PRPG!) + (0.15 × Ast%) + (0.10 × FTR%)
### College Offensive Efficiency Index
A metric focused on scoring efficiency and shot quality indicators, emphasizing true shooting percentage and efficiency-based performance measures.
- TS% x Usg%
### Two-Way Impact Score
A composite incorporating defensive activity, rebounding impact, and overall box impact metrics to evaluate all-around contribution.
- (0.40 × BPM) + (0.20 × D-Rtg) + (0.15 × Stl%) + (0.15 × Blk%) + (0.10 × D-PRPG)
### Balanced Prospect Score
A stability-adjusted composite designed to reward prospects who demonstrate strength across multiple dimensions rather than excelling in only one area. This score emphasizes balance across offensive, defensive, and efficiency components. Calculated by taking the mean of the Z-Scores of the BPM, Offensive Index Score, Two-Way Impact Score, and Usg%.

## Dashboard Highlights
- Top prospect rankings by Superstar Score
- Heatmap of standardized performance metrics across players
- Historical superstar benchmark reference lines
- Prospect vs benchmark scatter visualization
- Composite score comparisons across multiple impact dimensions

## Future Improvements
- Introduce weighting optimization for composite indices
- Explore clustering methods to identify archetype groupings
- Incorporate additional advanced metrics (playtype efficiency, on/off splits)
- Test regression-based approaches for predictive modeling
- Expand historical comparison group beyond current NBA superstars
