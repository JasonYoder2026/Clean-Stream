# User Acceptance Testing (UAT)

## Last Updated: 2/25/2026

---

# 1. Feature Overview

| Feature | Priority | Iteration | Client Facing (Y/N) |
|---------|----------|-----------|---------------------|
|Making Payments|High|1|Yes|
|Scanning Machine QR Codes|High|1|Yes|
|Loyalty Card|High|2|Yes|
|Machine Availability|High|2|Yes|
|Account Creation|High|2|Yes|
|Notifications for Laundry Finishing|High|3|Yes|
|Unlock doors after hours|High|4|Yes|
|Monthly Report|Medium|2|Yes|
|Request Refund|Medium|2|Yes|
|Find Locations on a Map|Medium|3|Yes|
|Light & Dark mode|Low|2|Yes|
|Account Management|Low|3|Yes|
|Loyalty Rewards|Low|4|Yes|

---

# 2. Acceptance Scenarios

## Feature: Making Payments
Users should be able to make payments to the loyalty card and individual machines.

### Scenario 1: Happy Path
**Given:** A user is logged in and has a debit/credit card

**When:** The user clicks a pay button

**Then:** The user can input card details and a successful transaction occurs.

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/45)

### Scenario 2: Error Handling
**Given:** The user is logged in and has a credit/debit card

**When:** The user clicks a pay button and an error occurs

**Then:** The user sees a popup with the error message and no transaction occurs

**Status:** Client accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/59)

### Scenario 3: Edge Case
**N/A**
---

## Feature: Scanning Machine QR Codes
User should be able to scan the machine QR code and be taken to the machines payment page.

### Scenario 1: Happy Path
**Given:** A user is logged in

**When:** The user scans the machine QR code

**Then:** The user is routed to the machine payment page and can pay for their laundry.

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/45)

### Scenario 2: Error Handling
**Given:** The user is logged in and has a credit/debit card

**When:** The user clicks a pay button and an error occurs

**Then:** The user sees a popup with the error message and no transaction occurs

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/59)

### Scenario 3: Edge Case
**N/A**

## Feature: Loyalty Card  
Users should be able to manage and use a digital loyalty card.

### Scenario 1: Happy Path
**Given:** A user is logged in and on the loyalty card page

**When:** They tap "Load card"

**Then:** They can make a payment and add money to their loyalty card balance

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/10)

### Scenario 1.5: Happy Path
**Given:** A user is logged in
**When:** They navigate to the loyalty card page

**Then:** They can see their loyalty card balance

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/10)

### Scenario 2: Error Handling
**Given:** A user is logged in and on the loyalty card page

**When:** The user attempts to make a payment to load the card and it fails

**Then:** A popup is show describing the error and saying no transaction occurred.

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/10)

### Scenario 3: Edge Case
**Given:** A user has a loyalty card balance exactly equal to the machine cost

**When:** The user makes a payment using the loyalty card

**Then:** The transaction succeeds and the balance becomes $0.00

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/10)

---

## Feature: Machine Availability  
Users should be able to view machine availability.

### Scenario 1: Happy Path
**Given:** A user is logged in and on the home screen

**When:** They select a location from the dropdown menu

**Then:** The user sees the machine availability for that location

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/56)

### Scenario 2: Error Handling
**Given:** A user has a session active 

**When:** They try to open the app to the loading screen without network connection

**Then:** The app doesn't load

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/56)

### Scenario 3: Edge Case
**Given:** A user selects a valid location that currently has no machines configured

**When:** The machine availability screen loads

**Then:** The user sees no machines are available at that location

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/56)

---

## Feature: Account Creation  
Users should be able to create an account.

### Scenario 1: Happy Path
**Given:** A user is on the signup screen

**When:** They click sign up with valid signup fields filled out

**Then:** They can verify their email and login

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/94)

### Scenario 2: Error Handling
**Given:** A user is on the signup screen

**When:** They click sign up with invalid signup fields filled out

**Then:** They see red text explaining which fields are filled out wrong

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/94)

### Scenario 3: Edge Case
**Given:** A user is on the signup screen

**When:** They enter a maximum-length valid name and email within allowed limits

**Then:** The account is created successfully without truncation or system error

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/94)

---

## Feature: Notifications for Laundry Finishing  
Users should receive notifications when laundry is finished.

### Scenario 1: Happy Path
**Given:** A user has paid for and started a machine

**When:** The machine is close to finishing

**Then:** The user gets a notification some minutes before the machine ends according to their user preference

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/84)

### Scenario 2: Error Handling
**Given:** A user has paid for and started a machine

**When:** The machine is close to finishing and the user has no network connection

**Then:** The user still receives the notification

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/84)

### Scenario 3: Edge Case
**Given:** A user has set their notification preference to 0 minutes before completion

**When:** The machine cycle finishes

**Then:** The user receives the notification exactly when the cycle ends

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/84)

---

## Feature: Unlock doors after hours  
Authorized users should be able to unlock doors after hours.

### Scenario 1: Happy Path
**Given:** A user has more than $20 on their loyalty card

**When:** The user presses "Unlock doors" and holds their phone to the door

**Then:** The door unlocks for the user

**Status:** In progress

**Evidence:** N/A

### Scenario 2: Error Handling
**Given:** A user has less than $20 on their loyalty card

**When:** The user presses "Unlock doors" 

**Then:** They receive a popup explaining they must have $20 on their card

**Status:** In progress

**Evidence:** N/A

### Scenario 3: Edge Case
**Given:** A user has exactly $20 on their loyalty card

**When:** The user presses "Unlock doors" and holds their phone to the door

**Then:** The door unlocks for the user

**Status:** In progress

**Evidence:** N/A

---

## Feature: Monthly Report  
Users should be able to view a monthly report.

### Scenario 1: Happy Path
**Given:** A user is logged in and has an account with transactions from a previous month

**When:** They navigate to the monthly report page

**Then:** They will see a list of spendings separated by category.

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/73)

### Scenario 2: Error Handling
**Given:** A user is logged in

**When:** They navigate to the monthly report page and the system fails to load data

**Then:** The user will see a nicely handled error message

**Status:** Not Implemented

**Evidence:** N/A

### Scenario 3: Edge Case
**Given:** A user is logged in and has no previous transactions

**When:** They navigate to the monthly report page

**Then:** The will see a message saying no previous transactions

**Status:** Not implemented

**Evidence:** N/A

---

## Feature: Request Refund  
Users should be able to request a refund.

### Scenario 1: Happy Path
**Given:** A user is logged in and has previous transactions

**When:** They navigate to the refund page and select a transaction, type a reason, and click submit

**Then:** The system starts the refund process and an admin recieves an email

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/74)

### Scenario 2: Error Handling
**Given:** A user is logged in and has previous transactions

**When:** They navigate to the refund page and select a transaction, type a reason, and click submit and the system fails

**Then:** They receive an error message explaining what went wrong

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/74)

### Scenario 3: Edge Case
**Given:** A user is logged in and does not have previous transactions

**When:** They navigate to the refund page, there are no transactions to choose from

**Then:** They are not able to submit the empty form

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/74)

---

## Feature: Find Locations on a Map  
Users should be able to find store locations on a map.

### Scenario 1: Happy Path
**Given:** A user is logged in and on the home screen  

**When:** They select a location from the dropdown menu

**Then:** The map autofocuses on a location

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/81)

### Scenario 2: Error Handling
**Given:** A user is logged in and on the home screen

**When:** The system fails to fetch location information

**Then:** The user receives an error message explaining what went wrong

**Status:** Internal Tested

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/81)

### Scenario 3: Edge Case
**Given:** A user is logged in and on the home screen

**When:** The user taps on the icon on the map

**Then:** The dropdown selects the location

**Status:** Not Implemented

**Evidence:** N/A

---

## Feature: Light & Dark mode  
Users should be able to switch between light and dark mode.

### Scenario 1: Happy Path
**Given:** A user is logged in and on the settings page

**When:** They tap the light/dark mode button

**Then:** The app toggles from one theme mode to the other

**Status:** Client Accepted

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/57)

### Scenario 2: Error Handling
**Given:** 

**When:** 

**Then:** 

**Status:** 

**Evidence:** 

### Scenario 3: Edge Case
**Given:** 

**When:** 

**Then:** 

**Status:** 

**Evidence:** 

---

## Feature: Account Management  
Users should be able to manage their account settings.

### Scenario 1: Happy Path
**Given:** A user is logged in and on the settings page

**When:** They navigate to edit account

**Then:** They can update their display name and email or delete their account

**Status:** Internal tested

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/91)

### Scenario 2: Error Handling
**Given:** A user is logged in and on the edit profile page

**When:** They try to edit profile information and the network/system fails

**Then:** They receive a popup error message explaining it failed

**Status:** Internal tested

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/91)

### Scenario 3: Edge Case
**Given:** A user is logged in and on the edit profile page

**When:** They try to edit profile information with invalid input

**Then:** They will get a popup error message and the system will not try to change their info

**Status:** Internal Tested

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/91)

---

## Feature: Loyalty Rewards  
Users should be able to earn and redeem loyalty rewards.

### Scenario 1: Happy Path
**Given:** A user is logged in and on the loyalty card page

**When:** The user spends $20 loading their loyalty card

**Then:** They earn $5 onto their loyalty card

**Status:** In progress

**Evidence:** N/A

### Scenario 2: Error Handling
**Given:** A user is logged in and on the loyalty card page

**When:** They try to load their card and the payment fails

**Then:** No rewards money is added to their card

**Status:** In progress

**Evidence:** N/A

### Scenario 3: Edge Case
**Given:** A user is logged in and on the loyalty card page

**When:** They load their card with $10 today and $10 tomorrow

**Then:** They earn $5 in rewards after the second transaction

**Status:** In Progress

**Evidence:** N/A

---
# 3. Client UAT Log

These tests are validated by the client.

| Date | Feature | Client Feedback | Action Required | Resolved (Y/N) |
|------|---------|-----------------|-----------------|----------------|
||Feature1||||

---

# 4. Open Acceptance Risks

## Risk1
- Risk:
- Mitigation Plan:

## Risk2
