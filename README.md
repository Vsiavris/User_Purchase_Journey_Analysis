# User Purchase Journey Analysis

## Project Overview
This project analyzes the time users spend from their first website visit to completing a purchase on the same day. The analysis focuses on understanding user behavior patterns, identifying anomalies, and providing actionable insights to optimize the conversion funnel.

> **Note**: Turing College requested this analysis for the educatinal purposes. It aim to understand how much time users spend from their first website visit until completing a purchase within the same day. The data base was provided by the College and is unavailable for third parties.

## Data Source
The analysis used the *turing_data_analytics.raw_events* table in BigQuery, containing time-stamped user events across the purchase funnel: page_view, view_item, add_to_cart, begin_checkout, add_payment_info, and purchase. The data spans from November 2020 to January 2021.

>**Note**: The raw database cannot be shared publicly. Sample query outputs are linked below. SQL queries are available in the accompanying [Product Analysis.ipynb](Product%20Analysis.ipynb) file.

## Key Findings

### 1. 📈 Anomalous Week 4 Behavior

Average purchase duration increased from ~68 minutes (Week 3) to ~111 minutes (Week 4)
Statistical significance confirmed with p-value of 0.00597

### 2. 💻 Platform-Specific Patterns

Users on "Other" operating systems experienced the longest purchase times (~190 min) during Week 4
Windows users had the second longest purchase times (~127 min) during Week 4

### 3. ✅ Improved Conversion Despite Longer Time

Week 4 conversion rate (1.53%) outperformed Week 3 (0.96%)
Longer engagement may correlate with higher purchase intent

### 4. 🔄 Churned User Behavior

Churned users took longer to view items but added to cart faster than converting users
Suggests hesitation during product exploration rather than at the decision stage

### 5. 📅 Day of Week Impact

Weekday sessions had longer purchase durations compared to weekends
Most pronounced during Week 4, with some weekdays exceeding 120 minutes


## Limitations

|Limitation|Impact|
|----------|------|
|1 Same-day analysis only| Multi-day consideration cycles are excluded|
|2 Short time frame (3 months)| Seasonal patterns may not be captured|
|3 No product category context| Can't correlate duration with item type or price|
|4 No external factor data| Marketing campaigns or site issues not accounted for|

## Recommendations
- Year-over-Year Analysis — Compare purchase durations for the same weeks in previous years to determine if Week 4's spike is seasonal
- Product Category Segmentation — Analyze whether longer purchase times correlate with specific product categories
- Promotional Impact Study — Investigate whether marketing campaigns during Week 4 influenced user behavior
- Channel Analysis — Segment by acquisition channel to understand if traffic source impacts conversion time
- Optimize for "Other" OS Users — Address potential UX or performance issues on less common operating systems
- Weekday Experience Optimization — Focus on improving the weekday user experience, where purchase times are consistently longer
