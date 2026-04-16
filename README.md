# Social Media Usage and Mental Health Analysis

## 1. Problem & User
**Problem:** Do people who spend more time on social media report higher levels of distraction, anxiety, sleep issues, and social comparison?  
**User:** Students, educators, mental health advocates, and digital wellness app developers.

## 2. Data Source
- **Source:** Anonymous online survey collected in April–May 2022.
- **Access Date:** April 16, 2026
- **Sample Size:** 478 social media users (filtered from 481 total responses)
- **Key Fields:** Age, Gender, Time spent on social media (categorical), Distraction score (1-5), Anxiety score (1-5), Sleep issues (1-5), Platforms used.

## 3. Methods
- **Data Cleaning:** Renamed columns, converted numeric values, removed missing data, filtered to social media users only.
- **Feature Engineering:** Mapped time categories to ordered categorical and numeric hours.
- **Analysis:** Distribution plots, boxplots, correlation heatmap, high/low usage group comparison, platform anxiety analysis, regression scatter plot.
- **Libraries:** pandas, numpy, matplotlib, seaborn.

## 4. Key Findings
1. More than 40% of respondents spend over 3 hours daily on social media.
2. Higher usage time correlates positively with distraction, anxiety, and sleep issues (r = 0.2–0.3).
3. High usage group (≥3.5h/day) scores 0.3–0.5 points higher on mental distress measures.
4. Platforms with highest average anxiety scores: TikTok (5.0), Pinterest (4.0), Facebook (3.6).
5. Distraction and anxiety are moderately correlated (r ≈ 0.4).

## 5. How to Run
1. Clone this repository:  
   `git clone https://github.com/your-username/social-media-mental-health-analysis.git`
2. Install dependencies:  
   `pip install pandas matplotlib seaborn jupyter`
3. Launch Jupyter Notebook and open `social_media_analysis_complete.ipynb`.
4. Run all cells sequentially.

## 6. Demo Video
[Click here to watch the demo](https://youtu.be/your-video-link)

## 7. Limitations & Next Steps
- **Limitations:** Cross-sectional data (no causality), self-reported measures, sample skewed towards young adults.
- **Next Steps:** Collect longitudinal data, include objective screen time, apply regression with demographic controls.

## 8. License
MIT
