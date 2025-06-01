This project focuses on exploratory data analysis (EDA) and visualization of football player attributes using data stored in a SQLite database. It highlights various technical and physical skills of players over time.

🎯 Project Objectives
Connect to and extract data from a SQLite database.

Analyze key player attributes (e.g., dribbling, passing, shooting).

Visualize attribute distributions using histograms and boxplots.

Draw meaningful insights from raw sports data without using machine learning.

## 📥 Download the Dataset

You can download the SQLite database file from Google Drive:

👉 [Download SQLite Database](https://drive.google.com/file/d/11VflZWG-avag58xMlyfcVlKmVaA-d9q2/view?usp=sharing)

*Note: The file is hosted on Google Drive and accessible to anyone with the link.*


🛠️ Technologies Used
Python 3

SQLite3 – Database connection

Pandas – Data manipulation and analysis

Matplotlib – Basic plotting

Seaborn – Advanced visualizations

Jupyter Notebook – Interactive coding environment

🗃️ Data Source
Database File: player_database.sqlite (or your actual filename)

Table Used: Player_Attributes

Key Columns:

player_name, date

Technical skills: dribbling, finishing, short_passing, etc.

Physical attributes: acceleration, stamina, strength, etc.

Goalkeeping: gk_diving, gk_reflexes, etc.

🔌 How to Use the Data
python
Copy
Edit
import sqlite3
import pandas as pd

# Connect to the database
conn = sqlite3.connect('player_database.sqlite')

# Load the player attributes
query = "SELECT * FROM Player_Attributes"
df = pd.read_sql(query, conn)

# Close the connection
conn.close()
📊 Features of the Analysis
Histograms showing the distribution of attributes like dribbling, finishing, short_passing.

Boxplots comparing attributes across dimensions (if available).

Handling missing data and basic data cleaning.

🚀 How to Run
Open the Jupyter Notebook (e.g., player_analysis.ipynb).

Make sure the SQLite file is in the same directory.

Install required libraries if not already installed:

bash
Copy
Edit
pip install pandas matplotlib seaborn
Run the cells to perform the analysis.

💡 Potential Extensions
Filter by date to analyze player development over time.

Compare players by position or nationality (if linked from other tables).

Add dashboards (e.g., with Plotly or Streamlit) for interactive exploration.
