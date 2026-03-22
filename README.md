# PROJECT TITLE 
Telemetry-Anomaly-Detection-using-NASA-Turbofan-Dataset

# PROJECT DESCRIPTION
This project focuses on analyzing telemetry sensor data from aircraft engines to detect degradation patterns and predict potential failure. 
The goal is to understand how sensor values change over time and identify early signs of abnormal behavior.

# Dataset Description
The dataset contains multiple engines (units), each with time-series sensor readings recorded over operational cycles. Each unit starts in a healthy state and gradually degrades until failure.

Each row represents one cycle of an engine and includes:
- Unit number (engine ID)
- Cycle number (time step)
- Operational settings(3)
- Sensor measurements(1-21)

- Each data files consist of multiple engine units (1-100). So it to be considered that the data is from number of engines of the same type. Each engine may have Initial Wear and manufacturing variation Which is unknown while working on the dataset and Considered normal(Not a fault condition) for this project. It is to be noted that the data is contaminated with sensor noise.

In the training dataset, the sensor data start from The healthy state of the engine, as it gradually degrades until failure. 
In the test dataset, The Cycle or test series and sometime prior to the Engine failure. 
The objective of this project is to predict the number of Remaining Operational Cycles(RUL), where the system could have been used before failure in the test dataset.

The data provided as a zip-compressed text file with 26 columns of numbers, separated by spaces. Each row is the summarization of data taken during a single operational cycle, each column is a different variable. The columns correspond to:
1)	unit number
2)	time, in cycles
3)	operational setting 1
4)	operational setting 2
5)	operational setting 3
6)	sensor measurement  1
7)	sensor measurement  2
...
26)	sensor measurement  26

# APPROACH
Steps followed in this project:
1. Data Understanding and Cleaning
2. Visualization of sensor trends for individual engines
3. Identification of informative sensors
4. Creation of Remaining Useful Life (RUL) as a degradation measure
5. Correlation analysis between sensors and RUL
6. Feature selection based on relevance to degradation

# KEY INSIGHTS
- Some sensors remain constant and are not useful
- Certain sensors show clear trends as the engine degrades
- Degradation is gradual and noisy, not sudden
- Correlation with RUL helps identify important features

# Future Work
- Build predictive models for RUL
- Implement anomaly detection on live-like data
