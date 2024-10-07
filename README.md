# **Summer Olympics Analysis Dashboard - Power BI Project**

## 1. Dashboard Overview

This Power BI dashboard provides an in-depth analysis of Summer Olympics data. It highlights key metrics such as total medals won by countries, gender-based medal analysis, and athlete participation. The dashboard offers insights into the performance of top-performing countries, the distribution of medals (gold, silver, bronze), and participation trends by gender.

## Dashboard Snaps :

### Home Page:

![Snap1](https://github.com/user-attachments/assets/586f9e99-6a7d-4ac4-b4dc-21c3a195ea61)

### Overview Page:

![Snap2](https://github.com/user-attachments/assets/6fa3967d-3ca3-4d72-bd71-8a9d9fef5f81)

### Athletes Page:

![Snap 3](https://github.com/user-attachments/assets/074723fa-7842-4aab-80bc-7e96f9072d1d)

### Country Page:

![Snap 4](https://github.com/user-attachments/assets/9ae90c9c-1bd0-4007-bf31-0a1a8e5f799d)

### Historical Page:

![Snap 5](https://github.com/user-attachments/assets/e633272c-9c7b-4bbe-abca-9d5f2018405e)


## 2. Key Visualizations

- **Total Medals by Country:** Bar charts display the total number of medals won by each country.
- **Medal Distribution by Gender:** Visualizations for male and female athletes showing the distribution of gold, silver, and bronze medals.
- **Top Performing Country:** Highlights the country with the highest medal tally.
- **Medals by Event:** Pie chart showing the share of total medals across different sports.
- **Athlete Participation:** Analysis of total athletes participating in the games, categorized by gender.
- **Gold Medals by Country:** Visualizing countries that have won the most gold medals.
- **Bronze, Silver Medals by Gender:** Split visuals showcasing how male and female athletes performed across different medal categories.

## 3. Measures and Calculations Used

| Measure Name                  | Data Type | Description                                                    |
|-------------------------------|-----------|----------------------------------------------------------------|
| **Total_Medals**               | Integer   | Total number of medals won by a country.                        |
| **Total_Gold_Medals**          | Integer   | Total gold medals won by a country.                             |
| **Total_Silver_Medals**        | Integer   | Total silver medals won by a country.                           |
| **Total_Bronze_Medals**        | Integer   | Total bronze medals won by a country.                           |
| **Total_Female_Athletes**      | Integer   | Number of female athletes participating in the event.           |
| **Total_Male_Athletes**        | Integer   | Number of male athletes participating in the event.             |
| **Silver_Female_Medals**       | Integer   | Silver medals won by female athletes.                           |
| **Bronze_Male_Medals**         | Integer   | Bronze medals won by male athletes.                             |
| **Top_Performing_Country**     | Text      | Country with the highest overall medal tally.                   |
| **Country_Highlight**          | Text      | Highlighting top countries based on medal performance.          |
| **Total_Athletes**             | Integer   | Total athletes participating in the Olympics.                   |

## 4. Steps to Build This Dashboard

### Step 1: Data Collection

The dataset used contains information such as total medals won, athlete gender, event, and countries.

- Ensure the dataset is clean and structured with no duplicates and missing values handled properly.
- Transform the dataset for analysis by creating calculated measures and fields as required.

### Step 2: Import Data into Power BI

- Import the dataset into Power BI Desktop using the “Get Data” option.
- Load the data and ensure relationships between tables are established.

### Step 3: Data Modeling

- Assign appropriate data types to each field, such as text for country names, integer for medal counts, and date fields where applicable.

### Step 4: Create Calculated Measures and Columns: Some of them are listed below

- Total_Gold_Medals = SUM('Medals'[Gold_Medals])
- Total_Silver_Medals = SUM('Medals'[Silver_Medals])
- Total_Bronze_Medals = SUM('Medals'[Bronze_Medals])
- Total_Athletes = SUM('Athletes'[Total_Athletes])
- Gold_Medals_Male = CALCULATE(SUM('Medals'[Gold_Medals]), 'Athletes'[Gender] = "Male")
- Gold_Medals_Female = CALCULATE(SUM('Medals'[Gold_Medals]), 'Athletes'[Gender] = "Female")
- Silver_Medals_Female = CALCULATE(SUM('Medals'[Silver_Medals]), 'Athletes'[Gender] = "Female")
- Bronze_Medals_Male = CALCULATE(SUM('Medals'[Bronze_Medals]), 'Athletes'[Gender] = "Male")


### Step 5: Visualizations

- Total Medals by Country**: Bar chart visual showing the distribution of total medals.
- Medal Distribution by Gender (Stacked Column Chart)
- Top Performing Country (Card Visualization)
- Medals by Sport (Pie Chart)
- Athlete Participation by Gender (Stacked Bar Chart)
- Gold Medals by Country (Bar Chart)
- Bronze and Silver Medals by Gender (Clustered Column Chart)


### Step 6: Filters and Slicers

- Add slicers to filter data based on country, gender, and specific sports for detailed drill-down analysis.
- Use slicers to toggle between different Olympic events and years for performance comparison.

## 5. Conclusion

This Power BI dashboard offers a comprehensive analysis of the Summer Olympics by providing various visualizations that focus on medals, countries, gender-based performance, and participation trends. By using measures and visualizations effectively, this dashboard delivers a clear and detailed understanding of Olympic performances over time, helping stakeholders make informed decisions and gain insights into global athletic trends.


 
