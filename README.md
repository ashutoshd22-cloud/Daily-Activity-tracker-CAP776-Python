# Daily Activity Tracker

## Overview

**Daily Activity Tracker** is a personal time-management and activity-monitoring project created as part of an **MCA academic assignment at Lovely Professional University (LPU)**.

The project uses an Excel-based daily activity log to record and organize how time is spent throughout each day. The collected information is intended to serve not only as a record of daily activities but also as a **dataset for future Python-based data analysis and visualization projects**.

The tracker focuses on several important areas of daily life, including:

* Sleep
* Fitness and physical activities
* Academic study
* Programming and coding
* Classroom attendance
* Other personal activities
* Daily mood/feeling
* Satisfaction level
* Energy level
* Daily notes and observations

By maintaining this data consistently, it becomes possible to analyze personal habits, identify patterns, and understand how different activities affect productivity, energy, and overall satisfaction.

---

## Project Objective

The primary objective of this project is to create a structured dataset representing daily activities over an extended period.

The collected data can later be used with **Python, Pandas, Matplotlib, Seaborn, and other data-analysis libraries** to perform tasks such as:

* Daily and weekly activity analysis
* Study-time analysis
* Coding-time analysis
* Sleep-pattern analysis
* Fitness tracking
* Class-attendance analysis
* Productivity analysis
* Mood and satisfaction analysis
* Energy-level analysis
* Time-distribution analysis
* Identification of unusual or highly productive days
* Correlation analysis between different activities

The project therefore acts as a foundation for future **Python programming, data analysis, data visualization, and potentially machine-learning projects**.

---

## Dataset Structure

The main dataset is maintained in an Excel workbook.

### File

```text
12601870.xlsx
```

The filename follows the registration-number format specified in the assignment instructions.

The workbook contains two main worksheets:

### 1. Instructions

This sheet contains the guidelines for maintaining the dataset, including:

* File-naming instructions
* Data-entry instructions
* Time-format requirements
* Description of each column
* Dropdown-value options
* Recommended data-entry practices

### 2. Daily Log

This is the primary dataset sheet where daily activities are recorded.

Each row represents **one day**, while each column represents a specific activity or characteristic of that day.

---

## Dataset Columns

| Column                     | Description                                                                                                |
| -------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Date**                   | Calendar date for the daily entry                                                                          |
| **Sleep (min)**            | Total amount of sleep obtained during the day/night                                                        |
| **Fitness (min)**          | Time spent exercising, walking, playing sports, doing yoga, or other physical activities                   |
| **Study (min)**            | Academic study or reading time excluding coding                                                            |
| **Coding (min)**           | Time spent programming, practicing code, working on projects, or performing programming-related activities |
| **Class (min)**            | Time spent attending scheduled lectures or laboratory sessions                                             |
| **Classes Attended**       | Number of classes attended during the day                                                                  |
| **Other Activities (min)** | Time spent on other activities such as hobbies, social activities, chores, entertainment, etc.             |
| **Total Tracked (min)**    | Automatically calculated total of the tracked time                                                         |
| **Free/Unaccounted (min)** | Automatically calculated remaining time out of 24 hours                                                    |
| **Day's Feeling**          | General feeling or mood of the day                                                                         |
| **Satisfaction Level**     | Level of satisfaction with the day                                                                         |
| **Energy Level**           | Overall energy level during the day                                                                        |
| **Notes**                  | Additional information explaining unusual events, observations, or circumstances                           |

---

## Time Format

All duration-based activities are recorded in **minutes** rather than hours.

For example:

```text
2.5 hours of study = 150 minutes
45 minutes of fitness = 45 minutes
8 hours of sleep = 480 minutes
```

Using a single unit makes the dataset easier to process mathematically and prevents inconsistencies when performing calculations in Python.

---

## Automatic Calculations

Two columns in the Daily Log are calculated automatically.

### Total Tracked Time

The **Total Tracked (min)** column calculates the total amount of recorded time from the activity categories.

Conceptually:

```text
Total Tracked =
Sleep
+ Fitness
+ Study
+ Coding
+ Class
+ Other Activities
```

### Free / Unaccounted Time

The **Free/Unaccounted (min)** column represents the remaining time in a 24-hour day.

```text
Free/Unaccounted =
1440 - Total Tracked
```

Since a complete day contains:

```text
24 × 60 = 1440 minutes
```

this calculation makes it possible to see how much time has not been assigned to one of the tracked categories.

---

## Categorical Data

The tracker also records qualitative information about each day.

### Day's Feeling

The available values are:

```text
Excellent
Good
Neutral
Low
Stressed
```

### Satisfaction Level

The available values are:

```text
Very Satisfied
Satisfied
Neutral
Unsatisfied
Very Unsatisfied
```

### Energy Level

The available values are:

```text
High
Medium
Low
```

These categorical fields will be particularly useful for future Python analysis because they can be converted into numerical or categorical representations.

---

## Example Daily Entry

An example entry currently present in the dataset contains:

| Activity         |      Time |
| ---------------- | --------: |
| Sleep            |   360 min |
| Fitness          |     0 min |
| Study            |   175 min |
| Coding           |    42 min |
| Class            |   210 min |
| Classes Attended |         3 |
| Other Activities |   120 min |
| Total Tracked    |   907 min |
| Free/Unaccounted |   533 min |
| Day's Feeling    |      Good |
| Satisfaction     | Satisfied |
| Energy           |       Low |

The accompanying note records additional context about the day.

This demonstrates how both **quantitative data** and **qualitative observations** are being collected together.

---

## Data Collection Method

The recommended approach is to update the tracker consistently, preferably at approximately the same time every day.

The original workbook recommends filling in the data around the end of the day so that the activities and observations are still fresh and can be recorded accurately.

Each day should have its own row.

For example:

```text
10-Aug-2026 → One row
11-Aug-2026 → One row
12-Aug-2026 → One row
...
```

This structure makes the workbook suitable for conversion into a tabular dataset for Python.

---

## Future Python Applications

One of the main purposes of collecting this information is to use the dataset in future Python projects.

The Excel dataset can be imported using **Pandas**:

```python
import pandas as pd

df = pd.read_excel("12601870.xlsx", sheet_name="Daily Log")
```

Once imported, the dataset can be analyzed programmatically.

### Possible Analysis

#### 1. Sleep Analysis

Analyze:

* Average sleep duration
* Minimum and maximum sleep
* Sleep consistency
* Relationship between sleep and energy
* Relationship between sleep and productivity

#### 2. Study Analysis

Analyze:

* Daily study duration
* Weekly study trends
* Most productive study days
* Average study time
* Study time versus satisfaction

#### 3. Coding Analysis

Analyze:

* Daily coding time
* Weekly coding trends
* Total coding hours
* Coding consistency
* Coding time versus energy level

#### 4. Fitness Analysis

Analyze:

* Frequency of physical activity
* Total fitness time
* Average fitness duration
* Fitness versus energy level
* Fitness versus overall satisfaction

#### 5. Academic Analysis

The dataset can also be used to analyze:

* Number of classes attended
* Total classroom time
* Study time outside class
* Relationship between class attendance and study time

#### 6. Mood and Energy Analysis

The categorical fields can be analyzed to determine patterns such as:

```text
Sleep → Energy
Fitness → Energy
Study → Satisfaction
Coding → Satisfaction
Sleep → Mood
```

---

## Possible Data Visualizations

The dataset can eventually be used to create visualizations such as:

* Daily time-distribution charts
* Weekly activity trends
* Sleep-duration graphs
* Study-time graphs
* Coding-time graphs
* Fitness trends
* Class-attendance charts
* Mood distribution charts
* Satisfaction distribution charts
* Energy-level distribution
* Activity comparison charts
* Correlation heatmaps

For example, a future Python project could produce a chart showing:

```text
Date
  │
  ├── Sleep
  ├── Study
  ├── Coding
  ├── Fitness
  ├── Classes
  └── Other Activities
```

This would provide a visual representation of how time is distributed throughout the dataset.

---

## Potential Future Machine Learning Applications

After collecting a sufficiently large amount of data, the dataset could potentially be used for introductory machine-learning experiments.

For example, the data could be explored to determine whether activity patterns can be used to predict:

* Energy level
* Satisfaction level
* General mood
* Productivity patterns

However, meaningful machine-learning analysis would require a substantially larger and cleaner dataset than a few days of observations.

---

## Technologies and Tools

The current project primarily uses:

* **Microsoft Excel / Excel-compatible spreadsheet software** — Data collection and storage
* **Python** — Future data analysis
* **Pandas** — Dataset manipulation
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Jupyter Notebook / VS Code** — Future analysis and experimentation

Additional Python libraries may be introduced as the project develops.

---

## Data Integrity Guidelines

To keep the dataset useful for future analysis:

1. Record durations consistently in **minutes**.
2. Add only **one row per day**.
3. Avoid changing automatically calculated cells.
4. Use the provided dropdown values for mood, satisfaction, and energy.
5. Enter dates accurately.
6. Record unusual circumstances in the **Notes** column.
7. Avoid leaving activity fields blank when the correct value is actually zero.
8. Maintain consistent data-entry practices throughout the collection period.
9. Keep the original workbook structure intact.
10. Back up the dataset regularly.

Using `0` instead of leaving an activity blank is particularly important when an activity was genuinely not performed.

For example:

```text
Fitness = 0
```

means no fitness activity was performed, whereas:

```text
Fitness = blank
```

could mean the information was forgotten or not recorded.

These two situations should not be treated as identical during data analysis.

---

## Project Significance

Although the current project is a simple daily activity tracker, the dataset provides a practical introduction to **real-world data collection**.

Unlike manually created example datasets, this project collects observations from actual daily activities. This makes it useful for learning the complete data-analysis workflow:

```text
Data Collection
       ↓
Data Storage
       ↓
Data Cleaning
       ↓
Data Processing
       ↓
Data Analysis
       ↓
Data Visualization
       ↓
Pattern Identification
       ↓
Future Prediction / ML
```

The project therefore serves as a bridge between basic spreadsheet-based data entry and more advanced Python-based data science workflows.

---

## Repository Structure

A possible GitHub repository structure for this project is:

```text
Daily-Activity-tracker/
│
├── README.md
│
├── 12601870.xlsx
│
├── data/
│   └── daily_activity.csv
│
├── python/
│   ├── data_cleaning.py
│   ├── data_analysis.py
│   └── visualization.py
│
└── notebooks/
    └── daily_activity_analysis.ipynb
```

The additional Python files and folders can be added later as the project evolves.

---

## Future Scope

The project can be expanded beyond simple data recording.

Possible future improvements include:

* Automated Excel-to-Python data import
* Automatic data cleaning
* Weekly and monthly reports
* Interactive dashboards
* Productivity scoring
* Sleep and energy analysis
* Activity correlation analysis
* Automated charts
* Statistical analysis
* Personal productivity insights
* Machine-learning experiments
* Interactive dashboards using tools such as Streamlit

The long-term goal can be to transform the initial spreadsheet into a complete **personal activity analytics system**.

---

## Academic Context

This project was assigned by the **LPU faculty** as part of the MCA coursework.

It provides practical exposure to:

* Structured data collection
* Spreadsheet-based data management
* Data organization
* Basic statistical thinking
* Python data processing
* Data visualization
* Dataset preparation for future programming projects

The project is intentionally structured so that the collected data can be reused in subsequent Python assignments and experiments.

---

## Current Status

**Status:** `In Progress`

The dataset is currently being populated with daily activity information.

Future updates will include additional daily records and Python-based analysis once sufficient data has been collected.

---

## Conclusion

The **Daily Activity Tracker** is more than a simple time log. It is designed as a continuously growing personal dataset that can be used to study daily routines, productivity, academic activities, coding practice, physical activity, sleep, mood, satisfaction, and energy.

By maintaining consistent records over time, the project can eventually evolve from an Excel-based assignment into a practical **Python data-analysis and visualization project**.

The collected dataset will provide the foundation for future experiments involving **Pandas, data visualization, statistical analysis, and machine learning**.
