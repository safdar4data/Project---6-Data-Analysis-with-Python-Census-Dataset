🇮🇳 India Census 2011 — Pandas Data Analysis

<p align="center">
  <b>Practical Pandas Data Analysis Project</b><br>
  <i>Working with India Census 2011 data using Python & Pandas</i>
</p>

📌 Project Overview

This project demonstrates practical Pandas Data Analysis techniques using the India Census 2011 dataset.

The notebook covers dataframe styling, filtering records, state-wise aggregation, religion-wise population analysis, worker analysis, index management, and adding prefixes/suffixes to column names.

🛠️ Technologies Used

🐍 Python

🐼 Pandas

📊 Data Analysis

🇮🇳 India Census 2011 Dataset

📓 Jupyter Notebook / Google Colab

📂 Dataset

Dataset: 6. India Census 2011.csv

The analysis uses columns such as:

District_name

District_code

State_name

Population

Hindus

Muslims

Christians

Sikhs

Buddhists

Jains

Male_Workers

📚 Analysis Questions & Solutions

1️⃣ How to hide the indexes of a DataFrame?

data.style.hide()

This hides the displayed DataFrame index when rendering the styled DataFrame.

2️⃣ How to set a caption / heading on the DataFrame?

data.style.set_caption("India Census 2011")

This adds India Census 2011 as the caption of the styled DataFrame.

3️⃣ Show records related to New Delhi, Lucknow, and Jaipur

data[data['District_name'].isin(['New Delhi', 'Lucknow', 'Jaipur'])]

Explanation

The isin() method filters the DataFrame and returns records where District_name matches any of the specified districts.

4️⃣ Calculate State-wise Population

A. Total Population by State

data.groupby('State_name')['Population'].sum().sort_values(ascending=False)

Explanation

groupby('State_name') groups records according to state.

['Population'] selects the population column.

.sum() calculates total population.

.sort_values(ascending=False) displays states from highest to lowest population.

B. State-wise Population by Religion

data.groupby('State_name')[
    ['Hindus', 'Muslims', 'Christians', 'Sikhs', 'Buddhists', 'Jains']
].sum().sort_values(by='Hindus')

This calculates the total number of people belonging to the listed religious categories for every state.

5️⃣ How many male workers were there in Maharashtra?

data[data.State_name == 'MAHARASHTRA']['Male_Workers'].sum()

Explanation

The code:

Filters records for MAHARASHTRA.

Selects the Male_Workers column.

Calculates the total using .sum().

6️⃣ How to set a column as the DataFrame index?

data.set_index('District_code')

This sets District_code as the DataFrame index.

Note: By default, set_index() returns a new DataFrame. To modify the original DataFrame directly, you can use inplace=True.

data.set_index('District_code', inplace=True)

7️⃣ Add a Suffix or Prefix to Column Names

A. Add a Suffix

data.add_suffix("_rightone")

This adds _rightone to the end of every column name.

B. Add a Prefix

data.add_prefix("lefttone_")

This adds lefttone_ to the beginning of every column name.

🎯 Skills Demonstrated

Skill

Pandas Technique

DataFrame styling

data.style

Hide index

style.hide()

Add caption

style.set_caption()

Filter records

isin()

Group data

groupby()

Calculate totals

sum()

Sort results

sort_values()

Set index

set_index()

Add suffix

add_suffix()

Add prefix

add_prefix()

🚀 How to Run the Project

1. Install Pandas

pip install pandas

2. Keep the CSV file in the same folder as the notebook

Project Folder/
│
├── 6. India Census 2011.csv
├── India_Census_2011_Analysis.ipynb
└── README.md

3. Import Pandas

import pandas as pd

4. Load the dataset

data = pd.read_csv("6. India Census 2011.csv")

5. Run the analysis

Execute the notebook cells in order to reproduce the analysis.

👨‍🏫 Trainer Profile

Md Safdar

Senior Trainer – Data Analytics
Intensive Institute

I am a Senior Trainer for Data Analytics with Intensive Institute, focused on helping learners develop practical skills in Python, Pandas, data analysis, visualization, and related data technologies.

📇 Contact Details

Name: Md Safdar

Designation: Senior Trainer – Data Analytics

Institute: Intensive Institute

Mobile: 9810845947

Email: safdar.ncpul@gmail.com

LinkedIn: www.linkedin.com/in/md-safdar-595449

📈 Learning Outcomes

After completing this practical exercise, learners can:

Work with CSV datasets using Pandas.

Filter DataFrame records based on conditions.

Use isin() for multiple-value filtering.

Group data using groupby().

Calculate totals using sum().

Sort analytical results.

Perform state-wise population analysis.

Analyze population across selected religious categories.

Set DataFrame indexes.

Customize DataFrame display using styling.

Add prefixes and suffixes to column names.

🌟 About This Project

This project is designed as a practical exercise for Data Analytics learners. It focuses on commonly used Pandas operations that are useful for real-world data cleaning, exploration, aggregation, and reporting.

Learn • Practice • Analyze • Grow 🚀

👨‍💻 Trainer

Md Safdar | Senior Trainer – Data Analytics | Intensive Institute

📱 9810845947
📧 safdar.ncpul@gmail.com
🔗 www.linkedin.com/in/md-safdar-595449

<p align="center">
  <b>🇮🇳 India Census 2011 Data Analysis using Pandas</b><br>
  Made for practical Data Analytics learning.
</p>
