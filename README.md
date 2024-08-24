# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
Developed by:karnan K
Reg no:212222230062
```
```
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('/content/baggagecomplaints.csv')
df.head()
print(df.columns)
df_grouped = df.groupby(['Airline', 'Year'])['Enplaned'].sum().reset_index()
plt.figure(figsize=(10,6))
for airline in df_grouped['Airline'].unique():
    df_airline = df_grouped[df_grouped['Airline'] == airline]
    plt.plot(df_airline['Year'], df_airline['Enplaned'], label=airline, marker='o')
plt.title('Airline Baggage Complaints Over Time')
plt.xlabel('Year')
plt.ylabel('Number of Complaints')
plt.legend()
plt.grid(True)
plt.show()
```


# OUTPUT:

![Screenshot 2024-08-24 090955](https://github.com/user-attachments/assets/10016a80-88ee-4ab1-942a-44b59bd5a792)


![Screenshot 2024-08-24 091009](https://github.com/user-attachments/assets/f1c9faaf-eeac-4096-845e-5f516898706d)



# RESULT:
Thus we have created the python code for plotting the time series of given data.
