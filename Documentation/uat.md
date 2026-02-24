# User Acceptance Testing (UAT)

## Last Updated:

---

# 1. Feature Overview

| Feature | Priority | Iteration | Client Facing (Y/N) |
|---------|----------|-----------|---------------------|
|Making Payments|High|1|Yes|
|Scanning Machine QR Codes|High|1|Yes|
|Loyalty Card|High|2|Yes|

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

**Status:** Tested

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

**Status:** Tested

**Evidence:** [PR](https://github.com/jamaki604/CleanStreamLaundryApp/pull/59)

### Scenario 3: Edge Case
...
**N/A**
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
