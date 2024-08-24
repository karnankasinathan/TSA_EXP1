### Name: Karnan K
### Reg no:212222230062
###  Date: 
# Ex.No: 01A PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
12Import pandas and matplotlib.
2.Load the CSV data into a DataFrame.
3.Display the first few rows and column names.
4.Group data by Airline and Year, summing Enplaned complaints.
5.Plot the number of complaints over time for each airline.
6.Add title, labels, legend, and grid to the plot.
7.Show the plot.
# PROGRAM:

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
