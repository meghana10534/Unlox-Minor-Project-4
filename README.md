\# 🚨 RedFlag – The Fraud Files

**RedFlag – The Fraud Files** is a comprehensive **SQL-based fraud detection, transaction monitoring, and financial risk analysis project** designed to identify suspicious transaction patterns in a simulated digital payment environment. The project demonstrates how large-scale transactional data can be analyzed using advanced SQL techniques to uncover abnormal behavior, investigate potential fraud, and generate meaningful risk indicators.

The project simulates a real-world **digital payment aggregator / FinTech transaction environment** containing approximately **200,000 transaction records**. These records represent different types of payment activities involving customers, merchants, transaction amounts, timestamps, locations, refunds, accounts, and other transaction-related attributes. The large dataset provides an opportunity to perform realistic transaction analysis and understand how fraud patterns can emerge within high-volume digital payment systems.

---

## 📌 Project Overview

With the rapid growth of digital payments, online transactions, cards, wallets, and electronic payment systems, the volume of financial transactions has increased significantly. While digital payments provide convenience and speed, they also create opportunities for fraudulent activities such as repeated small transactions, unusual transaction spikes, refund manipulation, account misuse, and geographically impossible transactions.

**RedFlag – The Fraud Files** addresses this problem through a **rule-based SQL fraud detection approach**. Instead of using Machine Learning algorithms or external fraud-detection APIs, the project relies primarily on SQL queries and database analysis to detect suspicious transaction behavior.

The central idea of the project is to transform raw transaction data into meaningful fraud indicators by applying predefined rules and identifying patterns that deviate from normal transaction behavior.

The project demonstrates that SQL is not limited to simple data retrieval. With advanced querying techniques, SQL can be used for **data exploration, anomaly detection, behavioral analysis, transaction monitoring, risk identification, and fraud investigation**.

---

## 🎯 Main Objective

The primary objective of RedFlag – The Fraud Files is to analyze a large transaction dataset and identify records, customers, merchants, or transaction patterns that may indicate potentially fraudulent activity.

The project focuses on:

* Detecting unusual transaction behavior.
* Identifying suspicious customer and account activity.
* Finding abnormal transaction frequency and amount patterns.
* Detecting potentially fraudulent refund behavior.
* Identifying unusual merchant and customer relationships.
* Analyzing transaction timing and geographical information.
* Creating rule-based fraud indicators using SQL.
* Generating query outputs that can be used for further investigation.
* Demonstrating the practical application of SQL in a FinTech environment.

---

## 💡 Problem Statement

Digital payment platforms process thousands or millions of transactions every day. Monitoring each transaction manually is difficult and time-consuming. Fraudsters may also perform transactions in ways that appear normal when viewed individually but become suspicious when multiple transactions are analyzed together.

For example, a customer making one small transaction may not appear suspicious. However, if the same account performs dozens of transactions within a few minutes, repeatedly performs transactions of similar amounts, or suddenly becomes active after a long period of inactivity, the combined behavior may indicate a potential fraud pattern.

Therefore, there is a need for a systematic approach to analyze transaction history and identify suspicious behavior.

**RedFlag – The Fraud Files** attempts to solve this problem by creating SQL-based rules that examine transaction patterns and flag potentially suspicious activities for further investigation.

---

# 🔍 Fraud Detection Scenarios

The project investigates multiple fraud scenarios, with each scenario representing a different type of suspicious transaction behavior.

### 1. Velocity Fraud

Velocity fraud focuses on unusually high transaction frequency within a short period of time.

The analysis identifies customers or accounts that perform an unusually large number of transactions within a specific time window. This can help identify automated transaction activity, compromised accounts, or rapid fraudulent purchases.

---

### 2. Card Testing

Card testing occurs when multiple small-value transactions are performed to determine whether a card or payment method is active before attempting larger fraudulent transactions.

The analysis looks for repeated low-value transactions associated with the same account or payment instrument and examines their frequency and timing.

---

### 3. Round-Amount Transaction Clustering

Fraudulent transactions may sometimes involve repeated round-number amounts such as ₹1,000, ₹5,000, or ₹10,000.

The project analyzes transaction amounts and identifies customers, merchants, or accounts that show an unusual concentration of round-value transactions.

---

### 4. Mule Accounts

A mule account may be used to receive or transfer funds on behalf of another party.

The project investigates transaction patterns involving accounts that receive money from multiple sources, transfer funds frequently, or show unusual inflow and outflow behavior.

By examining transaction relationships, SQL can help identify accounts that require additional investigation.

---

### 5. Refund Abuse

Refund-related fraud can occur when refund functionality is repeatedly misused.

The project analyzes refund records and transaction history to identify unusual refund frequency, repeated refund activity, abnormal refund amounts, or customers and merchants associated with suspicious refund behavior.

---

### 6. Just-Under-Threshold Transactions

Some suspicious activity may involve transactions deliberately structured just below a predefined transaction limit.

The project identifies transactions that repeatedly occur immediately below a threshold and analyzes whether such behavior is concentrated among particular customers or accounts.

This type of analysis can help identify potential attempts to avoid transaction limits or monitoring rules.

---

### 7. Dormant-Then-Active Accounts

An account that remains inactive for a long period and suddenly begins performing multiple transactions may require additional investigation.

The project compares historical transaction activity with recent activity to identify accounts that show significant behavioral changes after a period of dormancy.

---

### 8. Merchant Collusion

Merchant collusion analysis focuses on unusual relationships between customers, merchants, and transactions.

The project examines transaction patterns to identify merchants that may have abnormal transaction relationships, repeated interactions with particular accounts, or unusual concentrations of activity.

---

### 9. Velocity Spikes

Velocity spikes focus on sudden increases in transaction activity.

Instead of only looking at the total number of transactions, the project compares transaction behavior across time and identifies sudden increases that differ significantly from previous activity.

---

### 10. Geographic Impossibility

Geographic impossibility refers to transaction activity that may be physically difficult or impossible within the observed time interval.

For example, if transactions associated with the same customer occur in geographically distant locations within a very short time, the pattern may require investigation.

The project uses available geographic and timestamp information to identify such suspicious transaction sequences.

---

# 🛠️ Technologies Used

The project is primarily implemented using **SQL and MySQL**.

### Core Technologies

* **MySQL**
* **SQL**
* Relational Database Concepts
* Transaction Data Analysis
* Rule-Based Fraud Detection
* Analytical SQL

### SQL Concepts Used

The project makes extensive use of advanced SQL features, including:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `HAVING`
* `ORDER BY`
* `DISTINCT`
* `CASE WHEN`
* Aggregate Functions
* Subqueries
* Common Table Expressions
* Window Functions
* `LAG()`
* Conditional Filtering
* Date and Time Functions
* Multi-level Queries
* Joins
* Transaction Aggregation
* Pattern-Based Analysis

---

# 🧠 SQL-Based Analytical Approach

The project follows a structured analytical process.

### Step 1 – Dataset Understanding

The transaction dataset is first examined to understand its structure, columns, data types, and available information.

Important fields may include information related to:

* Transaction ID
* Customer
* Merchant
* Transaction amount
* Transaction timestamp
* Account
* Location
* Refund information
* Transaction status
* Payment information

Understanding these attributes is important because different fraud scenarios require different fields for analysis.

---

### Step 2 – Data Exploration

Initial SQL queries are used to explore the dataset and understand transaction distributions.

Examples include:

* Total number of transactions.
* Number of unique customers.
* Number of merchants.
* Minimum and maximum transaction amounts.
* Average transaction amount.
* Transaction activity over time.
* Distribution of transaction statuses.
* Refund frequency.
* Customer-level transaction counts.

This stage provides a foundation for designing meaningful fraud rules.

---

### Step 3 – Rule Definition

For every fraud scenario, specific logical conditions are defined.

For example:

```text
High transaction frequency
        ↓
Repeated small transactions
        ↓
Unusual amount patterns
        ↓
Suspicious refund behavior
        ↓
Sudden account activity
        ↓
Geographically unusual transactions
```

These conditions become SQL-based detection rules.

---

### Step 4 – SQL Query Implementation

Individual SQL queries are created for each fraud scenario.

Advanced SQL concepts are combined to analyze transaction behavior across different dimensions such as:

* Customer
* Merchant
* Account
* Amount
* Time
* Location
* Refund
* Transaction frequency

---

### Step 5 – Suspicious Activity Identification

The results of the fraud queries are examined to identify transactions or accounts that satisfy the defined rules.

The output can include:

* Suspicious transaction IDs.
* Customer IDs.
* Merchant IDs.
* Transaction amounts.
* Transaction timestamps.
* Number of transactions.
* Frequency indicators.
* Refund indicators.
* Location-related indicators.

---

### Step 6 – Result Interpretation

The final step is to interpret why a particular record or account was flagged.

The project does not simply identify a transaction as suspicious; it attempts to understand the **pattern or rule that caused the transaction to be flagged**.

This makes the analysis more transparent and easier to investigate.

---

# 📊 Analytical Features

One of the important features of the project is its ability to analyze transactions from multiple perspectives.

### Customer-Level Analysis

Customer transaction history can be analyzed to identify:

* High transaction frequency.
* Unusual spending behavior.
* Sudden activity changes.
* Repeated small transactions.
* Multiple merchant interactions.
* Unusual transaction locations.

### Merchant-Level Analysis

Merchant behavior can be analyzed using:

* Transaction volume.
* Average transaction value.
* Customer concentration.
* Refund patterns.
* Repeated transaction patterns.
* Unusual transaction activity.

### Time-Based Analysis

Time-based analysis helps identify:

* Transactions occurring within short intervals.
* Sudden transaction spikes.
* Dormant account activation.
* Repeated transactions during unusual periods.
* Rapid sequences of transactions.

### Amount-Based Analysis

Transaction amounts are analyzed to detect:

* Round-number transactions.
* Low-value testing transactions.
* Repeated amounts.
* Threshold-related patterns.
* Unusual transaction values.

### Geographic Analysis

Location information can be used to identify:

* Rapid transactions from distant locations.
* Unusual location changes.
* Potential geographic impossibility.
* Suspicious location-based activity.

---

# 🧮 Advanced SQL Techniques

The project provides practical experience with several advanced SQL concepts.

## GROUP BY and HAVING

These are used to aggregate transactions and identify customers or merchants satisfying specific conditions.

For example, transaction counts can be grouped by customer to identify accounts with unusually high activity.

## CASE WHEN

`CASE WHEN` is used to create logical fraud indicators based on transaction conditions.

It can categorize transactions as:

* Normal
* Suspicious
* High Risk Indicator
* Potential Fraud Pattern

depending on the defined business rules.

## Subqueries

Subqueries are used when one query depends on the result of another query.

They help perform multi-stage transaction analysis.

## Common Table Expressions

CTEs make complex queries easier to organize and understand.

They allow the analysis to be divided into logical steps before generating the final result.

## Window Functions

Window functions are especially useful for analyzing transaction history while retaining individual transaction-level records.

They can be used to compare transactions within customer or account groups.

## LAG()

`LAG()` is used to compare a transaction with a previous transaction.

This is particularly useful for:

* Time-gap analysis.
* Geographic movement
