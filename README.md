Titanic EDA Dashboard

This project performs an Exploratory Data Analysis (EDA) on the Titanic dataset using Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn.
It visualizes survival patterns based on key features like Passenger Class, Sex, Age, Fare, and Embarkation Port.

📂 Dataset

The dataset used is train.csv, which typically contains:

Passenger details (Age, Sex, Class, Fare, etc.)

Survival information (1 = Survived, 0 = Did not survive)

🛠️ Libraries Used

Pandas → Data manipulation and analysis

NumPy → Numerical operations

Matplotlib → Core data visualization

Seaborn → Enhanced and styled data visualization

Install dependencies using:

pip install pandas numpy matplotlib seaborn

📈 Exploratory Steps
🧾 Data Loading

Load the Titanic dataset using pd.read_csv('train.csv')

🔍 Initial Data Exploration

Display dataset info using .info()

Check for missing values

Summarize statistics with .describe()

View value counts for key features: Survived, Pclass, Sex, Embarked

📊 Visualization 1: Main Dashboard

Survival Count: Bar plot showing survivors vs non-survivors

Passenger Class vs Survival: Survival rates across travel classes

Sex vs Survival: Comparison of survival between males and females

Age vs Survival: Boxplot showing age distribution across survival status

Fare vs Survival: Boxplot comparing fare distributions

Correlation Heatmap: Correlations between numeric features

📉 Visualization 2: Additional Analysis

Age Distribution: Histogram with KDE for passenger ages

Fare Distribution: Histogram with KDE for ticket fares

Embarked vs Survival: Bar plot showing survival by embarkation port

Age vs Fare Scatterplot: Scatterplot showing relation between age and fare, colored by survival

🧩 Output

Two complete dashboards with multiple subplots

Highlights survival insights by demographics, class, and embarkation

Presents clear visual relationships between age, fare, and survival

🎯 Key Insights

👩 Women had higher survival rates compared to men

🛳️ First-class passengers had a better chance of survival

👶 Younger passengers and those who paid higher fares showed a slight survival advantage

📌 How to Run

Ensure train.csv is available in the same directory as your script.

Run the analysis:

python code.py
