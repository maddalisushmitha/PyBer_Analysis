# PyBer_Analysis

## Overview of PyBer Share Ride Analysis

Analyzing PyBer data so as to show summary of total weekly fares for each city type as it helps 
decision-makers at PyBer.

## Results:

### Results using summary DataFrame:

#### Code:

#Format the columns.
pyber_summary_df["Total Riders"] = pyber_summary_df["Total Riders"].map("{:,}".format)  

pyber_summary_df["Total Drivers"] = pyber_summary_df["Total Drivers"].map("{:,}".format)  


pyber_summary_df["Total Fares"] = pyber_summary_df["Total Fares"].map("${:,.2f}".format)  
pyber_summary_df["Average Fare per Ride"] = pyber_summary_df["Average Fare per Ride"].map("${:.2f}".format)  

pyber_summary_df["Average Fare per Driver"] = pyber_summary_df["Average Fare per Driver"].map("${:.2f}".format)  

![PS](https://github.com/maddalisushmitha/PyBer_Analysis/blob/main/analysis/Pyber.png)

#### Rural type:
- Total Riders are greater then drivers present but the average cost per driver is very high
#### Sububren type:
- When compared to urban total riders are greater than total  drivers and the average cost per driver is little high than Average fare per ride.
#### Urben type:
- Total rides are lesser than total drivers and  the average cost per driver is less than Average fare per ride.

- To summaries Suburban and Rural are making good business attracting customers than Urban  

###  Results using summary multiple-line chart:

#### Code:

#Creating multiple-line chart  
from matplotlib import style  
#Use the graph style fivethirtyeight  .
style.use('fivethirtyeight')  
pyber_data_resample_df.plot(figsize=(20,5))  
plt.ylabel("Fare($USD)")  
plt.title("Total Fare by City Type") 
plt.legend(loc ="center")  

![I](https://github.com/maddalisushmitha/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)

- Rural city type has constant Total Fare through the 4 months
- There were high demand from mid of February to April in all the three city types


## Summary

### Recommendations

	1. Attract drivers with incentives in the Rural areas as the total riders are more in number it might profit in the future even though the Average fare per driver is more.
	2. Attract customers by giving promotions as the fare per ride is more than the fare for driver and this helps to win over the competitors of Pyber
	3. Attract Customers in Suburban as riders per driver in less in number
