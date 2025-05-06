🏥 Hospitalized COVID-19 Patients Dashboard


This project presents an interactive data dashboard analyzing hospitalization outcomes for COVID-19 patients in Mexico. It was developed as part of the Build Fellowship (February Cohort), under the mentorship of Pratyrush Kundu, with Nancy Odhiambo as a student consultant.

The goal is to explore how demographic and comorbidity factors influence the severity and outcomes of COVID-19 cases using a well-structured exploratory data analysis, data modeling, and dashboard visualizations.

📊 Dashboard Highlights
Developed using Streamlit, the dashboard provides interactive insights across multiple dimensions:

1. Age and Outcomes Visualization
Violin and box plots show how age distribution correlates with outcomes.

Clear trends reveal increased ICU admissions, intubations, and death with older age.

2. Severity vs Outcome
Grouped bar chart compares patient severity levels (Mild, Moderate, Severe) against outcomes (Alive, Dead).

Moderate cases surprisingly had a higher death rate than severe ones indicating care disparities.

3. Correlation Analysis
Interactive heatmaps reveal variables that correlate negatively with patient survival.

Features like pneumonia, classification level, and comorbidities show strong relationships with mortality.

4. Comorbidity Influence
Heatmaps highlight co-occurrence patterns among comorbidities.

Diabetes and hypertension frequently co-occur and increase mortality risk.

5. Navigation Panel
Sidebar enables smooth navigation across: Home, EDA, Modeling, Insights, and Data Source sections.

📸 Dashboard Preview
You can add screenshots by dragging and dropping them in your GitHub repository under the images/ folder and referencing them here like this:

md
Copy
Edit
![Dashboard Overview](images/dashboard_overview.png)
![Age Distribution](images/age_distribution.png)
![Modeling Metrics](images/model_metrics.png)
Replace these filenames with yours. Example below (remove if not using yet):



🔍 Modeling & Analysis
Preprocessing: Handled missing values (97/98/99), outlier removal, and binary encoding.

Feature Engineering: Grouped classification levels and transformed comorbidity indicators.

Model Used: Logistic Regression

Accuracy: ~82%

ROC AUC: High

Odds ratios and feature contributions were interpreted to highlight clinical risks.

⚙️ Technologies Used
Tool	Purpose
Python	Core programming language
Pandas	Data cleaning and transformation
Streamlit	Dashboard development
Plotly	Interactive visualizations
Seaborn	Statistical graphics
SQLAlchemy	Database connectivity
PostgreSQL	Data storage & querying
Scikit-learn	Model training & evaluation
Git & GitHub	Version control and collaboration

🧪 Project Structure
bash
Copy
Edit
📁 Hospitalized-Covid_19-Patients-dashboard
├── EDA_in_streamlit.py       # Main Streamlit app
├── covid_data.csv            # Cleaned dataset
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation
└── .gitignore                # File exclusions
🔍 Data Quality Findings
Data Cleaning Challenges: Removed unknown values (97, 98, 99)

Outlier Management: Removed 6,053 age outliers (~3.24%)

Class Imbalance: Mortality rate was 36.4%, addressed using balanced modeling

⚠️ Clinical Risk Factors
Strongest Predictors:

Pneumonia

Diabetes-Hypertension combo

Age > 60

Unexpected Findings:

Asthma showed potential protective effect

Moderate cases had higher mortality than severe ones

🏥 Operational Applications
Clinical Support: 82% recall for mortality prediction

Resource Planning: ICU forecasting and identification of high-risk profiles

⚠️ Limitations
Lack of detailed lab/treatment data

Dataset includes hospitalized patients only

Potential underreporting for non-hospitalized fatalities

👥 Contributors
Nancy Odhiambo – Student Consultant, Data Science & Analytics

Pratyrush Kundu – Project Supervisor, Build Fellow

📌 Acknowledgment
The dataset used in this project was provided by the Mexican Government, covering clinical data on COVID-19 positive cases across the country.

🚀 Getting Started
bash
Copy
Edit
# Clone the repo
git clone https://github.com/Nancy-Odhiambo/Hospitalized-Covid_19-Patients-dashboard.git
cd Hospitalized-Covid_19-Patients-dashboard

# Install dependencies
pip install -r requirements.txt

# Run the dashboard
streamlit run EDA_in_streamlit.py
📬 Contact
For questions, feedback, or collaboration:

GitHub: Nancy Odhiambo

Email: odhiambn@mail.gvsu.edu
