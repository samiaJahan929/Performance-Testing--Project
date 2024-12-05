# Performance Testing


# Introduction : In the performance testing test project, I took two APIs.
1.Restful-Booker (Books API):
Purpose: Load and stress testing.
Test Setup:
Simulate varying loads using threads to test response times under different traffic conditions.
Use HTTP requests (GET, POST, PUT, DELETE) and validate responses with assertions.

2.Dmoney (Website Transaction API):
Purpose: API chaining for transactions (Deposit, SendMoney, Payment).
Test Setup:
Use CSV Data files to run dynamic transaction data.
Simulate multiple transactions using three threads to concurrently run Deposit, SendMoney, and Payment APIs in a chain.

This setup ensures both load testing and real-world transaction performance testing using JMeter.


# Technology Used
-Jmeter
-Postman


# Load and Stress Test Excel Report
For the Load test and Stress test Excel report checkout the link, you will be directed to Google sheet and can see the results there.
#Link : https://docs.google.com/spreadsheets/d/1JJYM3DkWfO0HgiYXKlvftrv8ZQnklS60NcbkBpLc8X8/edit?usp=sharing


# HTML Report Generate :
# Generated HTML report for Load Test
![image](https://github.com/user-attachments/assets/86e44040-2810-462e-8755-eb8d0905677b)


# Generated HTML report for Stress Test
![image](https://github.com/user-attachments/assets/7763c2ad-ec3c-43e9-87d4-b41a1d6e3c7a)

![image](https://github.com/user-attachments/assets/ba10795f-6a9a-4f2f-a9e8-f97768e2a02a)


# Generated HTML report for DMoney Jmeter Collection Test

![image](https://github.com/user-attachments/assets/b3bca432-4aee-4143-9cdc-d699c08f004d)
![image](https://github.com/user-attachments/assets/4e963e93-558c-4c90-9443-efc7bddc0dc5)







