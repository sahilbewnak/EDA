# 🚢 Titanic EDA Dashboard (Single Code)
# --------------------------------------
# Author: Sahil Bewnak
# Description: Visual EDA dashboard for Titanic dataset
# --------------------------------------

# 1️⃣ Import Libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import os

# 2️⃣ File Path (Your Exact Path)
file_path = r"C:\Users\bewna\Downloads\titanic\train.csv"

# 3️⃣ Load the Data
if not os.path.exists(file_path):
    print("❌ File not found! Please check path:", file_path)
    exit()
else:
    df = pd.read_csv(file_path)
    print("✅ Titanic dataset loaded successfully!\n")

# 4️⃣ Set Style
sns.set_theme(style="whitegrid", context="talk", palette="Set2")
plt.rcParams['figure.facecolor'] = 'whitesmoke'

# 5️⃣ Basic Info
print("📘 Dataset Info:")
print(df.info(), "\n")

print("📊 Summary Statistics:")
print(df.describe(), "\n")

# 6️⃣ Dashboard Layout
fig, axes = plt.subplots(3, 3, figsize=(20, 15))
fig.suptitle("🚢 Titanic Data Dashboard", fontsize=24, fontweight='bold')

# Chart 1: Survival Count
sns.countplot(ax=axes[0,0], data=df, x='Survived', palette='crest')
axes[0,0].set_title("Survival Count")

# Chart 2: Passenger Class vs Survival
sns.countplot(ax=axes[0,1], data=df, x='Pclass', hue='Survived', palette='viridis')
axes[0,1].set_title("Passenger Class vs Survival")

# Chart 3: Gender vs Survival
sns.countplot(ax=axes[0,2], data=df, x='Sex', hue='Survived', palette='coolwarm')
axes[0,2].set_title("Gender vs Survival")

# Chart 4: Age Distribution
sns.histplot(ax=axes[1,0], data=df, x='Age', bins=30, kde=True, color='teal')
axes[1,0].set_title("Age Distribution")

# Chart 5: Fare Distribution
sns.histplot(ax=axes[1,1], data=df, x='Fare', bins=30, kde=True, color='orange')
axes[1,1].set_title("Fare Distribution")

# Chart 6: Embarked vs Survival
sns.countplot(ax=axes[1,2], data=df, x='Embarked', hue='Survived', palette='pastel')
axes[1,2].set_title("Embarked vs Survival")

# Chart 7: Age vs Fare Scatter
sns.scatterplot(ax=axes[2,0], data=df, x='Age', y='Fare', hue='Survived', palette='cool', s=60, alpha=0.8)
axes[2,0].set_title("Age vs Fare (Colored by Survival)")

# Chart 8: Boxplot - Fare by Pclass
sns.boxplot(ax=axes[2,1], data=df, x='Pclass', y='Fare', palette='flare')
axes[2,1].set_title("Fare by Passenger Class")

# Chart 9: Heatmap (Correlation Matrix)
corr = df.select_dtypes(include='number').corr()
sns.heatmap(ax=axes[2,2], data=corr, annot=True, cmap='coolwarm', fmt=".2f", linewidths=0.5, square=True)
axes[2,2].set_title("Feature Correlation Heatmap")

plt.tight_layout(pad=3.0, rect=[0, 0, 1, 0.96])
plt.show()

# 7️⃣ Insights Summary
print("\n💡 Insights Summary:")
insights = [
    "1️⃣ Women had much higher survival rates than men.",
    "2️⃣ 1st-class passengers had better survival chances.",
    "3️⃣ Younger and wealthier passengers survived more often.",
    "4️⃣ Fare and Pclass are strongly related to survival.",
    "5️⃣ Passengers from Embarked C had higher survival rates."
]
for i in insights:
    print(i)

print("\n✅ Dashboard Analysis Completed Successfully!")
