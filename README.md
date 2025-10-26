# ✈️ Airlines Flight Data Analysis Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Library-Pandas-orange?logo=pandas)
![Seaborn](https://img.shields.io/badge/Visualization-Seaborn-9cf?logo=seaborn)
![Matplotlib](https://img.shields.io/badge/Plotting-Matplotlib-blueviolet)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Level](https://img.shields.io/badge/Level-Intermediate-brightgreen)

---

## 📘 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on an **Airlines Flights Dataset** containing 300,000+ records.  
The objective is to uncover insights about:
- Airline performance  
- Ticket pricing trends  
- Route patterns  
- Correlation between duration, days left, and price  

---

## 🎯 Objectives

- Analyze flight data to discover price trends  
- Compare airlines, routes, and travel classes  
- Visualize correlations between variables  
- Generate actionable business insights  

---

## 🧩 Dataset Information

| Feature | Description |
|----------|--------------|
| `airline` | Name of the airline |
| `flight` | Flight number |
| `source_city` | Origin city |
| `departure_time` | Category of departure time (Morning, Evening, etc.) |
| `stops` | Number of stops (non-stop, 1 stop, etc.) |
| `arrival_time` | Category of arrival time |
| `destination_city` | Destination city |
| `class` | Type of ticket (Economy/Business) |
| `duration` | Total travel time (in hours) |
| `days_left` | Days left for departure at the time of booking |
| `price` | Ticket price (in INR) |

---

## 🧰 Tech Stack & Libraries

| Tool / Library | Purpose |
|----------------|----------|
| 🐍 **Python** | Programming language |
| 🧮 **Pandas** | Data manipulation and analysis |
| 📊 **Matplotlib** | Data visualization |
| 🌈 **Seaborn** | Advanced visualization and aesthetics |
| ⚠️ **Warnings Filter** | To ignore unnecessary warnings |

---

## 🧾 Data Exploration Steps

1. **Data Loading & Inspection**
   - Checked data types, null values, and duplicates  
   - Verified dataset integrity (300,153 rows × 12 columns)

2. **Descriptive Statistics**
   - Used `df.describe()` and `df.describe(include="all")`

3. **Exploratory Data Analysis**
   - Count and distribution plots for:
     - Airlines  
     - Source & destination cities  
     - Departure & arrival times  
     - Stops and class types  

4. **Grouping and Aggregation**
   - Mean, Max, and Min price by airline, class, source, and destination  

5. **Correlation Analysis**
   - Heatmap for `duration`, `days_left`, and `price`

---

## 📈 Visualizations Included

| Visualization | Description |
|----------------|-------------|
| 🧮 Countplot | Distribution of airlines and classes |
| 🌆 Barplot | Source city vs airline counts |
| 🔥 Heatmap | Average, Max, Min prices across cities |
| 🕒 Time Analysis | Departure & Arrival time patterns |
| 💰 Correlation Matrix | Relationship between price, duration, and days_left |

---

## 💡 Key Insights

| Observation | Insight |
|--------------|----------|
| 🏆 **Top Airlines** | Vistara, Air India, and Indigo dominate flight volume |
| 💺 **Class** | Only Air India & Vistara offer Business class |
| 🚀 **Stops** | Indigo operates the most non-stop flights |
| 💸 **Price Trends** | Fares increase as `days_left` decrease |
| 🔗 **Correlation** | `Days_left` and `price` show strong negative correlation |
| 🌍 **Routes** | Delhi–Mumbai and Bangalore–Delhi are the most frequent |

---

## 📊 Correlation Heatmap Example

```python
plt.figure(figsize=(8,6))
sns.heatmap(df[['duration','days_left','price']].corr(), annot=True, fmt=".2f", cmap='coolwarm', linewidths=0.5)
plt.title("Correlation Matrix: Duration, Days Left, Price")
plt.show()
