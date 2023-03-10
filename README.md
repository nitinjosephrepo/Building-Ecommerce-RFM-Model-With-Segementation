# Using Recency, Frequency and Monetary Value (RFM) to Segement Retail Customers

## Objective
It is very important for companies to know their customers and understand their behavior well to be able to meet their needs and be successful. 
We will be using online retailer customer transactions. First, we will run *Cohort analysis and compute metrics such as Retention rate and Churn rate.* These metrics will allow us to understand customer trends. After that, we will compute Customer Lifetime Value (CLV) which is a measurement of how much a company expects to earn from an average customer in a lifetime. Then, we will *run Recency/Frequency/Monetary/Tenure segmentation and create easy to interpret segments with K-mean clustering*. 

## What is RFM?
Recency, frequency, monetary value (RFM) is a marketing analysis tool used to identify a firm’s best clients based on the nature of their spending habits.
An RFM analysis evaluates clients and customers by scoring them in three categories: how recently they’ve made a purchase, how often they buy, and the size of their purchases.

## Significance of RFM?

RFM analysis allows a comparison between potential contributors and clients. It gives organizations a sense of how much
revenue comes 
from repeat customers (vs. new customers), and which levers they can pull to try to make customers happier so they become repeat purchasers. 

#### Recency

 The more recently a customer has made a purchase with a company, the more likely they will continue to keep the business and brand in mind for 
 subsequent purchases. Compared with customers who have not bought from the business in months or even longer periods, the likelihood of engaging 
 in future transactions with recent customers is arguably higher.

Such information can be used to get recent customers to revisit the business and spend more. In an effort not to overlook lapsed customers,
marketing efforts might be made to offer them an incentive to resume buying. 

#### Frequency 

The frequency of a customer’s transactions may be affected by factors such as the type of product, the price point for the purchase, 
and the need for replenishment or replacement. If the purchase cycle can be predicted—for example, when a customer needs to buy more groceries—marketing 
efforts may be directed toward reminding them to visit the business when staple items run low. 

#### Monetary

Monetary value stems from how much the customer spends. A natural inclination is to put more emphasis on encouraging customers who spend the most 
money to continue to do so. While this can produce a better return on investment (ROI) in marketing and customer service, it also runs the risk of 
alienating customers who have been consistent but may not spend as much with each transaction. 

## Visualizing Active, Retention & Churn Rate

#### No. of Monthly Active Customers 


<img width="818" alt="Screenshot 2023-02-16 at 9 58 08 PM" src="https://user-images.githubusercontent.com/80999165/219538775-79571e7e-94c5-4c7d-b827-d97e3536b334.png">


#### Monthly Retention Rate 

<img width="816" alt="Screenshot 2023-02-16 at 9 58 00 PM" src="https://user-images.githubusercontent.com/80999165/219538840-c828b2f9-360d-4057-ac70-0e6196bc132d.png">


#### Monthly Churn Rate 

<img width="819" alt="Screenshot 2023-02-16 at 9 57 51 PM" src="https://user-images.githubusercontent.com/80999165/219538951-7012271e-383e-4aea-a781-30f37ed419cd.png">

## Use K-Means clustering to Segement Users into Behavourial Buckets

#### Choose between 3 cluster solution or 4 Cluster Solutions

<img width="1106" alt="Screenshot 2023-02-16 at 10 04 59 PM" src="https://user-images.githubusercontent.com/80999165/219539792-c4930c67-9109-4a70-9c02-e0c4fbd8e7d2.png">

4-segment solution is a better choice because it provides more details, and we can immediately see the difference in RFMT values of those segments. In order to compare and understand our segments, we will create a snake plot and calculate relative importance of segment attributes. The snake plot is a visualization technique plotting segments and their RFMT values on a line plot. Relative importance of segments is the difference between our segments and overall population

### We derive RFM for each customer and segement them into Loyal, Middle, New & Churned


<img width="450" alt="Screenshot 2023-02-16 at 10 04 16 PM" src="https://user-images.githubusercontent.com/80999165/219540416-4a9a0c31-a950-4526-b869-cb8ccc94d4bd.png">

## Compute and visualize relative importance of segment attributes

<img width="576" alt="Screenshot 2023-02-16 at 10 15 31 PM" src="https://user-images.githubusercontent.com/80999165/219540712-a7905878-fdcc-4f53-af69-b3ad64458815.png">


Zero is returned when cluster average = population average. As a ratio moves away from zero, the more important that attribute for defining a specific cluster compared to the population average. Thus, 'Monetary' is the most important attribute across three clusters except 'Churned' segment. 'Recency' is the least important for 'New' and 'Middle' clusters but the most important for 'Churned' segment. 'Frequency' is the third important attribute for 'Churned', 'Middle' and 'New' clusters and second important for 'Loyal' segment. 'Tenure' is the least important attribute for 'Churned' and 'Loyal' clusters, and second important for 'Middle' and 'New' segments.

## Conclusion
The Cohort analysis shows that the customers who had longer relationship with the business demonstrated better performance across all metrics. Thus, the overall mean retention is around 30%, but the customers in cohort 2010-12-01 had retention rate in the region of 32%-50%. Moreover, we can clearly see that in 12 months 50% of the customers returned for purchases. Customer Lifetime Value is 2937.14 USD. Now, we can use that data to calculate how much the company can invest in customer acquisition. Also, we clustered our data into four segments – ‘Loyal’, ‘Middle’, ‘New’ and ‘Churned’ representing different customer behavior across Recency, Frequency, Monetary and Tenure metrics. Those clusters can be used for targeting or other business applications. 
