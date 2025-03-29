# Mental-Health-Trends
Analyzing Mental Health Trends in the Tech Industry Using OSMI Survey Data

# Introduction
Objective: To analyze mental health trends in the tech industry using OSMI survey data.

Importance: Understanding mental health issues in the tech industry can help improve workplace policies, provide better support for employees, and reduce stigma around mental health.
To begin with, the OSMI survey dataset was loaded into the Python environment, and an initial examination of the data was performed. This step included displaying the first few rows of the dataset to understand its structure and the type of information it contained. Key features relevant to the analysis, such as demographic details, mental health history, work environment, and support structures, were identified. These features were used to explore the trends and correlations within the data, offering insights into the mental health landscape in the tech industry.
# Data Preprocessing
Next, data preprocessing was carried out to ensure the dataset was clean and ready for analysis. Missing values were handled by removing rows with essential data points missing in the Excel spreadsheet, and typos and other errors in the data were corrected.

[5 rows x 24 columns]

Column Names: Index(['Age', 'Gender', 'Country', 'family_history', 'treatment',
       'work_interfere', 'self_employed', 'remote_work', 'no_employees',
       'tech_company', 'benefits', 'care_options', 'wellness_program',
       'seek_help', 'anonymity', 'leave', 'mental_health_consequence',
       'phys_health_consequence', 'coworkers', 'supervisor',
       'mental_health_interview', 'phys_health_interview',
       'mental_vs_physical', 'obs_consequence'],
      dtype='object')
      
# Explanatory Data Analysis
Feature Selection for Analyzing Mental Health Trends in the Tech Industry
For this project, features that provide insights into demographic information, work environment, and support structures were selected. The key features considered were:
### Demographic Features
1.	Age: Can help identify trends across different age groups.
2.	Gender: To analyze trends across gender groups.
3.	Country: To see if there are geographical differences in mental health trends.
### Work Environment
1.	no_employees: To understand the impact of company size on mental health.
2.	remote_work: To see if remote work affects mental health.
3.	tech_company: To compare trends between tech and non-tech companies.
4.	self_employed: To compare trends between self-employed individuals and those employed by companies.
### Support Structures
1.	benefits: To analyze the effect of mental health benefits provided by employers.
2.	care_options: To see if having care options available impacts mental health.
3.	wellness_program: To analyze the impact of wellness programs.
4.	seek_help: To see if the encouragement to seek help affects mental health trends.
5.	anonymity: To determine if anonymity in seeking help impacts mental health.
6.	leave: Ease of taking leave.


![Dashboard 1](https://github.com/user-attachments/assets/a88ab0f1-e99d-459c-a420-d63ecd92c10c)
![Dashboard 1(2)](https://github.com/user-attachments/assets/46e2e25f-0705-4237-bfdd-dfc3dbe11896)


The next step involved defining the factors and indicators that are relevant to the analysis. For analyzing demographic factors, I identified three key variables: age, gender, and Country. These factors provide insight into the respondents' background. Additionally, two mental health indicators were chosen: treatment (whether the respondent sought treatment for mental health conditions) and work_interfere (whether mental health issues interfere with work). These indicators help in assessing the mental health status of respondents and their perceived impact on work.

# Chi-square Tests and Count Plots
To analyze the relationship between each demographic factor and mental health indicator, I performed chi-square tests for the categorical variables (gender and Country). The chi-square test is a statistical method used to determine if there is a significant association between two categorical variables. For each combination of demographic factor and mental health indicator, I calculated the chi-square statistic and p-value. 

**Chi-square test for Gender and treatment**: Chi2: 35.17977721574272, p-value: 3.006292294799283e-09

**Chi-square test for Gender and work_interfere**: Chi2: 13.967872481856382, p-value: 0.0029492115846069668

**Chi-square test for Country and treatment**: Chi2: 18.233131570634363, p-value: 0.03256313846821809

**Chi-square test for Country and work_interfere**: Chi2: 21.32470650896996, p-value: 0.7708493271629728

The chi-square tests reveal significant associations between Gender and both mental health indicators—treatment (Chi2: 35.18, p < 0.00000001) and work interference (Chi2: 13.97, p = 0.00295)—indicating that gender strongly influences treatment-seeking behavior and how mental health impacts work, with a stronger effect for treatment. There’s also a significant but weaker association between Country and treatment (Chi2: 18.23, p = 0.0326), suggesting country-level differences in treatment-seeking, but no association between Country and work interference (Chi2: 21.32, p = 0.7708), implying work interference is consistent across countries.

Additionally, I created count plots using Seaborn to visualize the distribution and relationship between these categorical factors and indicators. This helped in visually understanding the data patterns and verifying the statistical results.

![image](https://github.com/user-attachments/assets/ca2d1c61-97c4-4445-93d6-51e6dfdcb665)
![image](https://github.com/user-attachments/assets/5b5fab7a-ee7d-4d86-b14c-c492c7647c30)
![image](https://github.com/user-attachments/assets/78a70f35-b315-4ffc-aa82-a56ee16912b0)
![image](https://github.com/user-attachments/assets/f91c2ad8-73e7-4e9f-8f65-488f632a4fe2)


# Histograms for Numerical Data
For the numerical demographic factor age, I created histograms with KDE (Kernel Density Estimate) plots to visualize its distribution and relationship with the mental health indicators. Histograms provide a visual representation of the frequency distribution of a numerical variable, while KDE plots add a smoothed line that represents the density of the data points. By creating these plots, I could see how age is distributed among respondents and how it correlates with whether they sought treatment or felt that mental health issues interfered with their work.

![image](https://github.com/user-attachments/assets/393ee0ef-add3-4660-92a8-5a79126df633)
![image](https://github.com/user-attachments/assets/cf3170ee-f7a8-4eaf-adfb-0588fd030a29)

Correlation Heatmap
![image](https://github.com/user-attachments/assets/fb813f7f-0d47-4bf3-bcd2-d649795555e7)


Finally, I encoded the categorical variables into numerical codes to calculate the correlation matrix, which measures the strength and direction of the relationships between the variables. This step involved converting categorical data into numerical values that can be used in correlation calculations. I then plotted a heatmap to visualize these correlations, which provided a comprehensive overview of how demographic factors are related to mental health indicators. The heatmap used color coding to represent correlation coefficients, making it easier to identify strong and weak relationships between variables.

![image](https://github.com/user-attachments/assets/54fe84a5-0146-4f0e-813a-21a1325f1629)

![image](https://github.com/user-attachments/assets/8a67e673-9b2b-4d54-a186-c42eea07607c)


# Conclusion
By following these steps, I performed a detailed analysis of how demographic factors such as age, gender, and country impact mental health indicators in the dataset. The combination of statistical tests and visualizations provided a thorough understanding of the data, highlighting significant patterns and correlations.




