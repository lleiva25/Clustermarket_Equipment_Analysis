# Clustermarket Equipment Analysis
-----------------------------------------------------------------------------------------------------------------------------------
Purpose
-----------------------------------------------------------------------------------------------------------------------------------
Automate metrics for quicker insights regarding equipment usage from Clustermarket, a lab management system that produces .csv reports of equipment usage. 

-----------------------------------------------------------------------------------------------------------------------------------
Python Libraries
-----------------------------------------------------------------------------------------------------------------------------------

| Module |  Abb    | Reference |
| :---:   | :---: | :---: |
| Pandas | pd  | |
| pathLib | | Path   |
| sys |   | |
| matplotlib.pyplot | plt   | |
|ListedColormap ||  matplotlib.colors  |
| numpy | np  ||
| os |   ||
| seaborn | sns  ||
| datetime | dt  | datetime |

-----------------------------------------------------------------------------------------------------------------------------------
Plots Generated
---------------------------------------------------------------------------------------------------------------------------------
![Lab1_Chart_5 1](https://github.com/lleiva25/Clustermarket_Insight_Analysis/assets/140974405/8ba8759d-c158-4b22-b1da-6b37013c83d3)
![Lab1_Chart_5](https://github.com/lleiva25/Clustermarket_Insight_Analysis/assets/140974405/11590f8d-7606-4bd1-b131-74df5e939152)
![Lab1_Chart_7](https://github.com/lleiva25/Clustermarket_Insight_Analysis/assets/140974405/8f2a8729-46ed-4be8-bb9e-153b6628e241)
![Lab1_Chart_8](https://github.com/lleiva25/Clustermarket_Insight_Analysis/assets/140974405/a1ad521d-fe48-4252-a317-fc1f8ab94ac2)

-----------------------------------------------------------------------------------------------------------------------------------
 
Summary
----------------------------------------------------------------------------------------------------------------------------------
Based on the generated plots, we can identify which teams are utilizing the equipment in each laboratory, and the status of equipment at a glance to determine how to optimize laboratory processes.

-----------------------------------------------------------------------------------------------------------------------------------
Process
-----------------------------------------------------------------------------------------------------------------------------------
1. Dataset file paths were established then cleaned through the following steps:
    - Removing rows with declined bookings
    - Selecting only the necessary columns:
                'Equipment ID',
                'Status',
                'Equipment Name',
                'Room',
                'Requester Name',
                'Booking Category',
                'Requested At',
                'Start Time',
                'Duration (minutes)',
                'Requester Group Name',
                'Notes')
    - Concert columns containing time elements to timeframe format
    - Rename the following entries in Booking Category to 'Unplanned': 'Breakdown', 'Repair' & 'Other
    - Replace the employee name with their department
      
2. Data analysis was done via .groupby() & pivot_table() attribute. Seaborn module was used to create quick tables in .png format
   
3. Plotting data utilizing Matplotlib  through vertical and horitzontal bar plots. 

-----------------------------------------------------------------------------------------------------------------------------------
Future Development
----------------------------------------------------------------------------------------------------------------------------------- Optimize code by utilizing vectorization and for-loops to generate outputs for all rooms
- Incorporating Clustermarket API into the code when released
-----------------------------------------------------------------------------------------------------------------------------------
