# Performance Testing Using Jmeter

# Content 
- [Introduction](#Introduction)
   - [Restful-Booker (Booking API)](#restful-booker-booking-api)
   - [Dmoney (Website Transaction API)](#Dmoney (Website Transaction API))
- [Technology Used](#Technology-Used)
- [Test Case scenario for Booking API ](#TestCasescenarioforBookingAPI)
   - [Login)](#Login)
   - [Create Booking)](#CreateBooking)
   - [Search Booking)](#SearchBooking)
   - [scenario)](#scenario)


# Introduction 

In the performance testing test project, I took two APIs.

<h3>1. Restful-Booker (Booking API):</h3>

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
 Add the following properties to the Header Controller : 

```console

Accept: */*
```

- <h4>Login </h4>
- <h4>URL : https://restful-booker.herokuapp.com/auth</h4>
- <h4>Request Body :</h4>
```console
{
"username": "admin",
"password": "password123"
}
```

- <h4>Create Booking </h4>
- <h4>URL : https://restful-booker.herokuapp.com/booking</h4>
- <h4>Request Body :</h4>
```console
{
"firstname": "Generate Random FirstName",
"lastname": "Generate Random LastName",
"totalprice": Generate random amount,
"depositpaid": true,
"bookingdates": {
"checkin": "2024-01-01",
"checkout": "2024-01-02"
}
}
```
- <h4>Search Booking </h4>
- <h4>URL : https://restful-booker.herokuapp.com/booking/<booking_id&gt; </h4>

<b> Perform Performance testing for the following scenario: </b>

- 120,000 users over a 12-hour period log in, create a booking, and search for the booking. 
- Used a Gaussian Random Timer for simulating realistic user behavior
- Conducted load tests with increasing durations (5, 10, and 20 minutes)
- Conducted stress tests to identify the server's bottleneck throughput
- Generated HTML and Excel reports for both load and stress tests

# Test Case scenario for DMoney Booking API 
- Set up scenarios for deposits, send money, and merchant payments
- Used dynamic data from CSV files to simulate real-life transactions
- Added assertions to ensure transaction success
- Created a multi-threaded environment with a ramp-up period for realistic simulation

# How to Run the Test

This guide provides step-by-step instructions for setting up and running performance tests using Apache JMeter.

- Download and Install latest version of "Apache JMeter"
- Extract the archive to your preferred directory
- Ensure JDK is Installed
   - Verify JDK is installed by running:
     ```bash
     java -version
     ```
   - Install JDK if it is not already available on your system.
- Place the `.jmx` test plan files and `.csv` test data files in a dedicated directory.
- Open the `.jmx` files in JMeter

<h4>Test Setup for Booking API</h4> 

- Ensure URLs are Accessible.
- Review and adjust the random data generators in the test plan to match booking details requirements.

<h4>Test Setup for Dmoney API</h4> 

- The following `.csv` files with valid test data:
     - `deposit.csv`
     - `sendMoney.csv`
     - `payment.csv`
- Update the **Header Manager** in the test plan with a valid API token for authorization.

<h4>Run the Tests</h4> 

- Start Apache JMeter from the terminal 
- Open the `.jmx` file, such as `booking.jmx` or `dmoney.jmx`.
- Click the **Start** button to execute the test.
- Monitor test progress in the ***View Results Tree*** or ***Summary Report***.
- Save the test results as an HTML report for analysis.


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







