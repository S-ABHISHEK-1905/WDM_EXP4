## EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
## DATE: 12/3/24
## AIM: 
To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
## Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
## Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

## Program:
```
# read the data
import pandas as pd
visitor_df = pd.read_csv('/content/clustervisitor.csv')

# Perform segmentation based on characteristics (e.g., age groups)
age_groups = {
    'Young': visitor_df['Age'] <= 30,
    'Middle-aged': (visitor_df['Age'] > 30) & (visitor_df['Age'] <= 50),
    'Elderly': visitor_df['Age'] > 50
}

for group, condition in age_groups.items():  
    visitors_in_group = visitor_df[condition] 
    print(f"Visitors in {group} age group:")
    print(visitors_in_group)

```
## Output:
![image](https://github.com/S-ABHISHEK-1905/WDM_EXP4/assets/66360846/3f70e905-ef61-4414-b729-e63512624027)

## Visualization:
```
# read the data
import pandas as pd
visitor_df = pd.read_csv('/content/clustervisitor.csv')

# Perform segmentation based on characteristics (e.g., age groups)
age_groups = {
    'Young': visitor_df['Age'] <= 30,
    'Middle-aged': (visitor_df['Age'] > 30) & (visitor_df['Age'] <= 50),
    'Elderly': visitor_df['Age'] > 50
}

for group, condition in age_groups.items():  
    visitors_in_group = visitor_df[condition] 
    print(f"Visitors in {group} age group:")
    print(visitors_in_group)

```
## Output:
![image](https://github.com/S-ABHISHEK-1905/WDM_EXP4/assets/66360846/43e0b8b8-0e07-4184-9fe3-f712c9adcf03)


## Result:
Thus the Implementation of Cluster and Visitor Segmentation for Navigation patterns is executed successfully.
