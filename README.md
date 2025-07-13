# Mess Hall Crowd Prediction – Hackathon Project

---

##  Problem Statement

The mess hall experiences irregular crowd levels — some weeks it's overcrowded, others underutilized. Despite fixed meal times and a standard menu cycle, the causes behind this fluctuation aren't well understood.

This project analyzes historical mess data to uncover patterns, identify key influencing factors, and build a predictive model to estimate weekly mess crowd levels accurately.

---

##  Dataset Overview

The dataset includes **6435 weekly records** with the following features:

| Column                  | Description                                      |
|-------------------------|--------------------------------------------------|
| `Mess_ID`              | Unique ID of the mess hall                       |
| `Date`                 | Start date of the week                           |
| `Weekly_Crowd`         | Total number of dinners served that week         |
| `Is_Holiday`           | If that week had a holiday (1 = Yes, 0 = No)     |
| `Temperature`          | Avg temperature of the week (Fahrenheit)         |
| `Menu_Score`           | Popularity score of the menu                     |
| `Event_Intensity_Index`| Level of campus activities/events                |
| `Stress_Level`         | Academic workload index                          |

---

##  Exploratory Data Analysis (EDA)

-  **Holidays** → Significant drop in mess crowd  
   **High Menu Score** → Attracts more students  
-  **Academic Stress** → Slightly reduces mess usage  
-  **Event Intensity** → More events = Slightly higher crowd  
-  **Mess ID** → Some mess halls are consistently busier

>  6 clean graphs were created using `seaborn` to visualize these insights (see `/graphs` folder).

---

## Model: Random Forest Regressor

- Trained on features:  
  `Mess_ID`, `Is_Holiday`, `Temperature`, `Menu_Score`, `Event_Intensity_Index`, `Stress_Level`
  
- **Evaluation Metrics:**
  - 📈 R² Score: `0.9685` 
  - 📉 MSE: `~1,025,000`

> The model predicts weekly crowd with high accuracy and can be used in real scenarios to manage food and staff planning.

---

##  Files Included

| File/Folder      | Description                          |
|------------------|--------------------------------------|
| `notebook.ipynb` | Main Jupyter notebook with code      |
| `report.pdf`     | Final report (EDA, insights, model)  |
| `video/link.txt` | Link to explanation video            |
| `graphs/`        | All generated graphs/images          |

---

##  Final Recommendations

- Use predictions weekly to plan **food quantity and staff**
- Reduce **waste** by avoiding over-preparation during low turnout weeks
- Improve **menu planning** based on expected crowd
- Use holiday and stress level patterns for better scheduling

---

##  Demo Video

 [Click here to watch the video](https://drive.google.com/your_demo_link)  
*Explains the approach, graphs, and model output in 2 minutes.*

---

## Technologies Used

- Python (Numpy,Pandas, Seaborn, Scikit-learn, Matplotlib)
- Jupyter Notebook
- GitHub for version control
- Google Drive (for video)
