# Performance Testing Using Jmeter


# Introduction 

In the performance testing test project, I took two APIs.

<h3>1. Restful-Booker (Books API):</h3>

- Purpose: Load and stress testing.
  
- Test Setup:
   - Simulate varying loads using threads to test response times under different traffic conditions.
   - Use HTTP requests (GET, POST, PUT, DELETE) and validate responses with assertions.

<h3>2.Dmoney (Website Transaction API):</h3>

- Purpose: API chaining for transactions (Deposit, SendMoney, Payment).
  
- Test Setup:
  - Use CSV Data files to run dynamic transaction data.
  - Simulate multiple transactions using three threads to concurrently run Deposit, SendMoney, and Payment APIs in a chain.

This setup ensures both load testing and real-world transaction performance testing using JMeter.


# Technology Used
- Java Development Kit (JDK)
- Apache Jmeter
- Postman


# Test Case scenario for Booking API 
<h3> Create a JMeter Collection of Login API, Create booking , Search booking HTTP requests</h3>
 Add the following properties to the Header Controller

```console

Accept: */*
```

- <h3>Login </h3>

- <h3>Pre Request Script</h3>
URL : https://restful-booker.herokuapp.com/auth


```console
{
"username": "admin",
"password": "password123"
}
```


  

- Configured API for login, booking creation, and booking search in Jmeter
- Used a Gaussian Random Timer for simulating realistic user behavior
- Conducted load tests with increasing durations (5, 10, and 20 minutes)
- Conducted stress tests to identify the server's bottleneck throughput
- Generated HTML and Excel reports for both load and stress tests



# Load and Stress Test Excel Report
For the Load test and Stress test Excel report checkout the link, you will be directed to Google sheet and can see the results there.

- [View load and stress test report](https://docs.google.com/spreadsheets/d/1JJYM3DkWfO0HgiYXKlvftrv8ZQnklS60NcbkBpLc8X8/edit?usp=sharing)


# HTML Report Generate :
 <h3> Generated HTML report for Load Test </h3>
 
![image](https://github.com/user-attachments/assets/86e44040-2810-462e-8755-eb8d0905677b) 


 <h3>Generated HTML report for Stress Test </h3>

![image](https://github.com/user-attachments/assets/7763c2ad-ec3c-43e9-87d4-b41a1d6e3c7a)


![image](https://github.com/user-attachments/assets/ba10795f-6a9a-4f2f-a9e8-f97768e2a02a)


<h3>Generated HTML report for DMoney Jmeter Collection Test</h3> 

![image](https://github.com/user-attachments/assets/b3bca432-4aee-4143-9cdc-d699c08f004d)

![image](https://github.com/user-attachments/assets/4e963e93-558c-4c90-9443-efc7bddc0dc5)







