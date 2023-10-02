## &ensp;&ensp;&ensp;&ensp;&ensp;Credit Risk Analysis (Power BI)

The report was made from a synthetic credit risk dataset.
Data was first uploaded to a Azure SQL Database then queried from Power BI.

### Question:

The company built a machine learning model to decide to allow or deny customers loans.
The project is for you to analyze this dataset and make sure the stakeholders and engineering teams have a more reason-based understanding of the data on which the model was trained on.
Task is the find the key factors that correlate with loan defaults.


### Insights:

After our analysis, it was found that the top factors strongly associated with loan defaults are:
- Loan Grade: G grades are associated with 80% defaults. A, B, C grades are particularly less riskier than the rest.
- Income: People with an income lower than $20k have 80% chance of defaulting. Higher income is usually associated with less defaults.
- Home ownership: Renting one's home, as well as customers falling into the 'other' category, is associated with roughly 2x more risk of default than having a mortgage or owning a home.
- Loan to Income %: The higher % of a person's income a loan accounts for, the higher the risk of default. When Loan to Income % gets higher than ~35%, the probability of defaulting hovers between 60-80% depending on the individual.
- Past Defaults History: People who defaulted in the past have roughly 2 times more risk of defaulting on their current loan.

Additional findings:
- Interest rates: the influence of interest rates on defaults is present but quite weaker than other factors.
- Loan intent: "Home improvement" is the only loan intent where the average non-defaulted loan is of higher amount than the defaulted loans. 


### Recommendations:

- According to the findings above, manual heuristic checks could be put in place to make sure that certain specific outlier decisions made by the ML model regarding accepting/denying certain loans can be reviewed by humans for confirmation (for example, the ML model decides to deny a loan with a Loan to Income % lower than 15%). Heuristics could be designed based on those 5 factors: Loan Grade, Income, Home Ownership, Loan to Income % and Past Default history.
- These heuristics must first be tested in a development environment and tuned to only send an alert on rare outlier decisions.
- The "home improvement" loans could become a category of loans where higher amounts could be allowed compared to other loan intents.

<br>

*Power BI report:*
<br>
<p align="center">
  <img src="https://github.com/AlexandreGarito/pbi_demo_2/blob/main/images/demo2_0001.jpg" width="33%" />
  <img src="https://github.com/AlexandreGarito/pbi_demo_2/blob/main/images/demo2_0002.jpg" width="33%" />
  <img src="https://github.com/AlexandreGarito/pbi_demo_2/blob/main/images/demo2_0003.jpg" width="33%" />
  <img src="https://github.com/AlexandreGarito/pbi_demo_2/blob/main/images/demo2_0004.jpg" width="33%" />
  <img src="https://github.com/AlexandreGarito/pbi_demo_2/blob/main/images/demo2_0005.jpg" width="33%" />
  <img src="https://github.com/AlexandreGarito/pbi_demo_2/blob/main/images/demo2_0006.jpg" width="33%" />
</p>  
