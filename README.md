# Summary of findings and the analysis process

1. Specify a target group of users. Justify your choice using the sample data
The purpose is to identify users who take advantage of the sale instead of paying full price. Therefore, the first analysis is to detect all IDs for this type of payers, and then compare this type of users with users who purchased. By merging ‘spenddevnts’ and ‘iaps’ tables, users who purchased and those who did not have been identified. Results are follows:
•	Users who purchased: 1181 unique user IDs (6.5% of total users): Payers
•	Users who did not purchase: 16887 unique user IDs (93.5% of total users): No_payers 


2. Specify a test and evaluation protocol. How long should the test run? How will you know if you have successfully increased revenue?
Users who purchased is defined as ‘Payers’, and users who did not purchase defined as ‘No_payers’. This analysis examines the duration from the first event to the last spend event between Payers and No_payers. Where i is an unique user.

{Duration}_i={Last\ spend\ event}_i-{First\ spend\ event}_i

Result 1: Payers player games longer than No_payers. This explains that most of No_payers received the promotion benefits for playing, and then they stopped playing once they could not receive the benefits anymore. The median duration for No_payers is 0 hours, and it is around 118 hours for Payers. This means that most of No_payers only spent 1 time to earn germs, and there was no more spending activity. 
  To understand how Payers purchased the game product, it is necessary to investigate when they purchased. The duration from the first spending activity to the first time to purchase was analyzed using the following equation. Where k is an unique Payer

{Duration_purchase}_k={First\ time\ to\ purchase}_k-{First\ spend\ event}_k


Result_2: In Figure 2, It shows the median value of Duration_purchase. For example, in US, the median hours of duration from the first time users earned gems to the first time they purchased game products is approximately 10 hours. It means that half of users earned gems and then purchased game products after 10 hours elapsed. In addition, this value is different by countries. Based on these results, the company can test the following protocol. 
1. Using the No_payers IDs identified in this analysis
2. Identify their first time to earned gems
3. After a certain hour (based on different countries), if they do not purchase the game products, stop providing promotion to them. For example, if an No_payer does not purchase the game products after 10 hours from the first time he/she earns gems in U.S. Then stop providing the promotion to this person.
4. Calculate the total revenue lost from all these No_payers. If the value has decreased, it indicates that the company’s revenue has increased. 
 

