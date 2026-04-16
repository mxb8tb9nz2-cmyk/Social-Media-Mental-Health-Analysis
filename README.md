# Project Reflection – Social Media & Mental Health Analysis

## Project Overview
In this project, I analyzed a survey dataset to investigate the relationship between social media usage time and several mental health indicators: distraction, anxiety, sleep issues, and social comparison. The goal was to answer whether heavier social media users report worse mental health outcomes. I used Python with pandas, matplotlib, and seaborn to clean the data, perform exploratory analysis, and generate visualizations.

## What Went Well
The data cleaning process was straightforward: I renamed columns, converted numeric types, dropped missing values, and filtered to keep only social media users. I then transformed the `Time_Spent` variable into an ordered categorical and a numeric hour format, which allowed me to create meaningful comparisons. The visualizations – including time distribution, boxplots, correlation heatmap, and regression plot – clearly showed positive associations between usage time and mental distress. The high vs. low usage group comparison (≥3.5h/day vs. ≤2.5h/day) revealed consistent differences of 0.3–0.5 points on a 5-point scale. Platform analysis (using only the first platform per user) indicated that TikTok, Pinterest, and Facebook users had the highest average anxiety scores.

## Challenges Faced
One challenge was handling the "platforms" column, which contained multiple platforms per user. Exploding the column would have double-counted anxiety scores, so I opted to take only the first platform as the primary platform. This is a reasonable simplification but may miss nuances for users who use multiple platforms equally. Another minor issue was the initial warning about chained assignment in pandas; I resolved it by using `.loc` for assignment.

## Limitations
The dataset is cross-sectional, so we cannot infer causality. All variables are self-reported, which may introduce bias (e.g., social desirability). The sample is not representative of the general population (mostly young adults). Also, the platform analysis assumes the first platform is the most important, which may not always be true.

## Future Improvements
Given more time, I would:
- Apply multiple linear regression to control for age, gender, and other confounders.
- Collect objective screen time data (e.g., from smartphone logs).
- Use a more robust method for platform analysis, such as indicator variables for each platform.
- Include a longitudinal follow-up to explore directionality.

## AI Use Declaration
I used **ChatGPT (OpenAI)** on **April 16, 2026** in the following ways:
- Generated initial code for data cleaning, column renaming, and conversion of time categories.
- Helped debug the pandas chained assignment warning.
- Provided the structure and template for this reflection and the README file.
- Suggested improvements for visualizations (e.g., adding titles, axis labels, saving figures).

All AI-generated code was reviewed, understood, and adapted by me. The final analysis, interpretation of results, and business recommendations are my own work. I also manually adjusted chart colors, labels, and saved output files to ensure clarity and relevance.

## Professional Practice
This project reinforced the importance of reproducible analysis and clear communication. Writing a thorough README and documenting code with Markdown cells in the notebook made the work accessible to others. In the future, I will also include a `requirements.txt` file and consider using version control from the start.

## Conclusion
Overall, the analysis supports the hypothesis that heavier social media use is associated with poorer mental health indicators. While causal claims cannot be made, the findings offer actionable insights for digital wellness applications.
