Data Product: The Impact of Social Media on Mental Health & Anxiety

Author: Yuquan.Deng
Student ID: 2472588

---

1. Problem & Target User
In the digital age, excessive screen time and the algorithms of social media platforms are increasingly linked to mental health issues, particularly among younger generations. 
This data product investigates two core questions: 
1. Which specific social media platforms induce the highest levels of anxiety? 
2. Is there a statistical correlation between a user's distractibility and their anxiety score? 

Target Users: Mental Health App Developers, Digital Wellbeing Marketers, and Tech Companies seeking data-driven insights to design healthier digital features (e.g., "Focus Modes").

2. Data
Source: Kaggle (Social Media and Mental Health Survey Dataset)
Access Date:May 2024
Key Fields Analyzed (Renamed for programmatic access):
         `7. What social media platforms do you commonly use?` ➡️ `Platform`
        `12. On a scale of 1 to 5, how easily distracted are you?` ➡️ `Distraction_Score`
        `13. On a scale of 1 to 5, how much are you bothered by worries?` ➡️ `Anxiety_Score`

3. Methods & Technical Execution
This project was implemented using Python in a Jupyter Notebook environment. Key steps include:
1.  Data Cleaning & Type Conversion: Handled missing values (`NaN`) and forced survey score columns into float formats using `pd.to_numeric()` to resolve `TypeError` during calculations.
2.  Advanced Data Transformation: The raw `Platform` column contained multi-choice answers separated by commas (e.g., *"Facebook, Instagram, TikTok"*). I used string splitting and the pandas `.explode()` function to restructure the data, ensuring accurate single-platform analysis.
3.  Visualization & Statistical Modeling: Built a horizontal bar chart to rank platform anxiety levels, and a Seaborn linear regression plot (with `jitter` applied to prevent discrete data overplotting) to analyze correlations.

4. Key Findings & Business Insights
Platform Impact: Users of short-video and infinite-scroll platforms (such as TikTok and Snapchat) reported the highest average anxiety scores. Conversely, older and text/community-based platforms (like Facebook and Reddit) ranked lower on the anxiety scale.
The Distraction-Anxiety Link: The OLS regression line reveals a strong positive correlation between how easily users are distracted and their level of worry/anxiety. 
Business Recommendation: Mental health apps should implement a mandatory "Screen-Time Intervention" or "Focus Mode" feature that triggers mindfulness prompts when users exhibit high-distraction usage patterns.

5. How to run
1. Download the `social_media_data.csv` and the `ACC102_Mini_Assignment.ipynb` notebook.
2. Ensure both files are stored in the same local directory.
3. Open the notebook in Jupyter or VS Code.
4. Run the notebook cell by cell. 
Required libraries: `pandas`, `matplotlib`, `seaborn`.*

6. Product Demo Video 🎬
[👉 Click here to watch the 3-minute Video Presentation](这里放你传到B站或网盘的视频链接！！！别忘了填！！！)

7. Limitations & Next Steps
Limitations: The dataset relies on self-reported scores (Likert scale 1-5), which can be subjective. Furthermore, *correlation does not imply causation*; we cannot definitively conclude whether distraction causes anxiety or if pre-existing anxiety leads to distractibility.
Next Steps:Future iterations of this product could integrate real-time screen-time API data (e.g., Apple Screen Time) rather than relying on user estimates to build a more robust predictive model.


🤖 AI Disclosure Statement
In accordance with academic integrity guidelines, Generative AI (ChatGPT) was utilized strictly as a coding assistant in this project. 
Specifically, when facing a `TypeError` during data conversion, the AI guided me to use `pd.to_numeric()`. I also used AI to learn the `.explode()` method to properly handle the comma-separated strings in the survey data. Finally, AI provided the foundational syntax for adding `jitter` to the Seaborn regression plot. All business logic, problem definition, and video presentation narratives were formulated entirely independently. All codes were verified and successfully executed by myself.
