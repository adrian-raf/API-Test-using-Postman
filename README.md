# Simple Grocery Store API Testing

This project features automated API testing for the Simple Grocery Store system using Postman and Newman. The project covers comprehensive functional End-to-End (E2E) testing and negative scenarios to ensure API reliability.

## Tech Stack & Tools
* **API Testing Tool:** Postman
* **Test Runner:** Newman (CLI)
* **CI/CD:** GitHub Actions
* **Reporting:** Newman HTML Extra Reporter

## Test Scenarios
The collection is organized into two primary categories:

**1. Positive Testing (Functional & Business Logic)**
* Health Check: Verifying API status and availability.
* Checkout Workflow Simulation: Creating a new cart, adding items, dynamically updating quantities (using Path Variables), and removing items.
* Authentication: Registering an API client to retrieve a Bearer Token.
* Order Management: Creating and managing customer orders.

**2. Negative Testing (Error Validation & Security)**
* Authentication Validation: Testing for Missing Headers.
* Security Checks: Validating Invalid Tokens (ensuring 401 Unauthorized responses).
* Input Validation: Testing Invalid Inputs (incorrect category parameters, exceeding maximum/minimum limits).

## How to Run Tests Locally

### Prerequisites
Ensure you have Node.js installed on your machine.

### Steps
1. Clone the repository:
   ```bash
   git clone [https://github.com/adrian-raf/API-Test-using-Postman.git](https://github.com/adrian-raf/API-Test-using-Postman.git)

2. Install Newman and the HTML Extra Reporter:
   ```bash
   npm install -g newman newman-reporter-htmlextra

3. Execute the tests:
   ```bash
   newman run collection.json -e environment.json -r htmlextra
