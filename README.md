🏥 **Hospitalized COVID-19 Patients Dashboard**

![COVID-19 Banner](https://www.amprogress.org/wp-content/uploads/2020/03/Microbes-1.jpg)

This project presents an interactive data dashboard analyzing hospitalized patients outcomes for COVID-19 patients in Mexico. 

It was developed as part of the Build Fellowship (February Cohort) under the mentorship of Pratyrush Kundu with Nancy Odhiambo as a student consultant.

The goal was to explore how demographic and comorbidity factors influence the severity and outcomes of COVID-19 hospitalized cases using a well-structured exploratory data analysis data modeling and dashboard visualizations.

📊 **Dashboard Preview & Highlights**


![Dashboard Overview](images/overview.png)

![](images/Data_set.png)

![Visualizations](images/violin.png)

*Age Distribution Analysis*

Age is a critical factor in COVID-19 outcomes. Our analysis reveals:

- Median age: 56.0 years (IQR: 43.0-67.0)
- Mortality by age: Patients who died were significantly older (median 62.0 years) compared to survivors (median 51.0 years)
- Comorbidity age patterns: Patients with pneumonia averaged 56.5 years versus 52.0 years for those without

![](images/cooccurence.png)

*Comorbidity Analysis*
Key findings about pre-existing conditions in our hospitalized patients:

*Most common comorbidity*: pneumonia at 60.5% prevalence
Diabetes-Hypertension combo: Present in 23.4% of fatal cases
Pneumonia impact: Mortality rate jumps from 25.0% to 43.8% when present

*Clinical Insight*: The diabetes-hypertension combination occurs in 33,788 patients (18.1% of cohort), and 47.2% of these patients had fatal outcomes - significantly higher than the baseline 36.4% mortality rate.

![](images/severity.png)

*Critical Finding*: Moderate cases (classification 2) show a 100.0% mortality rate - higher than severe cases (classification 3) at 43.5%. Potential explanations include:

- More aggressive treatment protocols for severe cases
- Possible under-monitoring of moderate cases
- Classification system limitations

![Modeling Metrics](images/modeling.png)

Since the project is mainly concerned with the outcome of patient based on whether the patient had a pre existing condition like asthma, diabetes, hpertension, copd e.t.c the model was trained to evaluate Logistic Regression model to predict the likelihood of a patient dying if a feature is set to Yes that is 1 and output its accuracy, precision, recall and F1-score.From the predictions the health care workers are able to understand the critical need to care for patients based on their pre existing conditions

🔍 **Modeling & Analysis**

- Preprocessing: Handled missing values (97/98/99), outlier removal, and binary encoding.
- Feature Engineering: Grouped classification levels and transformed comorbidity indicators.
- Model Used: Logistic Regression
- Accuracy: ~82%, ROC AUC: High
- Odds ratios and feature contributions were interpreted to highlight clinical risks.

⚙️ **Technologies Used**

*Tool Used*

Python, Pandas, Streamlit, Plotly, Seaborn, Scikit-learn, Git & GitHub	

🧪 **Project Structure**

📁 Hospitalized-Covid_19-Patients-dashboard
├── EDA_in_streamlit.py       
├── covid_data.csv            
├── requirements.txt         
├── README.md                 
└── .gitignore                

🔍 **Data Quality Findings**

- Data Cleaning Challenges: Removed unknown values (97, 98, 99)
- Outlier Management: Removed 6,053 age outliers (~3.24%)
- Class Imbalance: Mortality rate was 36.4% addressed using balanced modeling

⚠️ **Clinical Risk Factors**

*Strongest Predictors to outcome being death*:

- Pneumonia
- Diabetes-Hypertension combo
- Age > 60
- Clasiffication_final (Moderate category)

*Unexpected Findings*:

Asthma showed potential protective effect

Moderate cases had higher mortality than severe ones

🏥 **Operational Applications**

Clinical Support: 82% recall for mortality prediction

Resource Planning: ICU forecasting and identification of high-risk profiles

⚠️ **Limitations**

Lack of detailed lab/treatment data

Dataset includes hospitalized patients only

Potential underreporting for non-hospitalized fatalities

👥 **Contributors**

*Nancy Odhiambo* – Student Consultant, Data Science & Analytics

*Pratyrush Kundu* – Project Supervisor, Build Fellow

📌 **Acknowledgment**

The dataset used in this project was provided by the Mexican Government, covering clinical data on COVID-19 positive cases across the country.

🚀 **Getting Started**

# Clone the repo

git clone https://github.com/Nancy-Odhiambo/Hospitalized-Covid_19-Patients-dashboard.git
cd Hospitalized-Covid_19-Patients-dashboard

# Install dependencies

pip install -r requirements.txt

# Run the dashboard

streamlit run EDA_in_streamlit.py

📬 **Contact**

For questions, feedback or collaboration:

GitHub: *Nancy Odhiambo*

Email: *odhiambn@mail.gvsu.edu*
