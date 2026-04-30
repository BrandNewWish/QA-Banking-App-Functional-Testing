# QA Project – XYZ Bank Functional Testing

## Overview
This project contains functional test cases for a demo banking application (XYZ Bank).  
It focuses on validating core banking features such as customer management, account creation, deposits, withdrawals, and transaction history.

---

## Scope
- Functional testing of banking workflows  
- Positive and negative test cases  
- End-to-end user flows  
- Data validation and business rules
  

## FR1 – Add Customer

### TC-01 – Adding a customer (happy path)
**Preconditions:** User is logged in as Bank Manager  

**Steps:**
1. Click “Add Customer”
2. Enter First Name: Rafał, Last Name: Mentor
3. Enter Post Code: 12-345
4. Click “Add Customer”
5. Open Customers list  

**Expected Result:**
- Form opens successfully  
- Fields accept input  
- Customer is added successfully  
- Customer appears in list  

---

### TC-02 – Adding a customer (negative path)
**Preconditions:** User is logged in as Bank Manager  

**Steps:**
1. Click “Add Customer”
2. Enter First Name and Last Name
3. Leave Post Code empty
4. Click “Add Customer”
5. Open Customers list  

**Expected Result:**
- Post Code field shows validation error  
- Customer is not created  
- Customer does not appear in list  

---

## FR2 – Open Bank Account

### TC-03 – Opening account (happy path)
**Preconditions:** Bank Manager logged in  

**Steps:**
1. Click “Open Account”
2. Select Customer: Hermione Granger
3. Select Currency: Dollar
4. Click Process  

**Expected Result:**
- Account is created successfully  
- Confirmation message appears  
- Account available for customer login  

---

## FR3 – Customer Login

### TC-04 – Customer login (happy path)
**Steps:**
1. Click “Customer Login”
2. Select Hermione Granger
3. Click Login  

**Expected Result:**
- Customer dashboard opens  
- Accounts and actions visible  

---

## FR4 – Deposit

### TC-05 – Deposit (positive)
**Steps:**
1. Click Deposit
2. Enter 10
3. Click Deposit  

**Expected Result:**
- Balance increases  
- Success message displayed  

---

### TC-06 – Deposit (negative)
**Steps:**
1. Enter -10
2. Click Deposit  

**Expected Result:**
- Transaction rejected  
- Balance unchanged  

---

## FR5 – Withdrawal

### TC-07 – Withdrawal (positive)
**Steps:**
1. Enter 100
2. Click Withdraw  

**Expected Result:**
- Balance decreases  
- Success message displayed  

---

### TC-08 – Withdrawal (negative)
**Steps:**
1. Enter 5007
2. Click Withdraw  

**Expected Result:**
- Transaction rejected  
- Balance unchanged  

---

## FR6 – Transaction History

### TC-09 – Transaction history
**Steps:**
1. Click Transactions  
2. Verify entries  

**Expected Result:**
- Transactions listed chronologically  
- Credit = Deposit  
- Debit = Withdraw
