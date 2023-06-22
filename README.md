# Telco_Customer_Churn_Prediction

Machine Learning approach in predicting customer churns out or not.

## Context
A Telco company would like to acquire customers that uses the company's services for a long term. But, there seems to be a lot of customers that wants to use the company's services. From that line of customers, the company would like to obtain information on whether a customer wants to use the company's services for a long time or just for a short period of time.

## Business Problem
The company would like to increase revenue by reducing financial losses, especially in expenses given towards customer. Therefore, the company would like the Customer Relationship Management (CRM) to minimize the losses in those areas. As a data scientist of the company, the CRM division would like to analyze the data on customers that churns. They would like to know which customers would churn out form the company as well as its characteristics.

Throughout the company's existence, they assumed that all customers woulud eventually churn out. Therefore the company would create expenses that are useless.

## Metric Evaluation
In analyzing the expenses of the company, the metrics used would be a confussion matrix.

- False Positive: predicted churn, but actually not churn
  - Consequences:
    Customer predicted to churn out, which meant that the company needs to spend on retention cost, such as discount, certain facilities, and other special treatments. But the customer doesn't churn out, therefore the retention cost the company must spend would be useless.
- False Negative: predicted not churn, but actually churn
  - Consequences:
    Customer not predicted to churn out, which meant that the company did nothing in maintaning that customer. But eventually that customer churns out, therefore the company must spend more expenses in acquisition cost which is 5x more than retention cost.

Therefore, the most unfavorable cost would false negative. By that assumption, the metric used would be f2 score.

## Data Understanding
| #   | Column                            | Dtype   | Description                                                   |
|-----|-----------------------------------|---------|---------------------------------------------------------------|
| 0   | Dependents                        | object  | Whether the customer has dependents or not.                   |
| 1   | Tenure                            | int64   | Number of months the customer has stayed with the company.    |
| 2   | OnlineSecurity                    | object  | Whether the customer has online security or not.              |
| 3   | OnlineBackup                      | object  | Whether the customer has online backup or not.                |
| 4   | InternetService                   | object  | Whether the client is subscribed to Internet service.         |
| 5   | Device Protection                 | object  | Whether the client has device protection or not.              |
| 6   | TechSupport                       | object  | Whether the client has tech support or not.                   |
| 7   | Contract                          | object  | Type of contract according to duration.                       |
| 8   | PaperlessBilling                  | object  | Bills issued in paperless form.                               |
| 9   | MonthlyCharges                    | float64 | Amount of charge for service on monthly bases.                |
| 10  | Churn                             | object  | Whether the customer churns or not.                           |
