# Simple Grocery Store API Testing

Automated API testing for the Simple Grocery Store system using Postman and Newman.
This project covers end-to-end functional scenarios and negative/error validation to ensure API reliability.

## Tech Stack and Tools

- API Testing Tool: Postman
- Test Runner: Newman (CLI)
- CI/CD: GitHub Actions
- Reporting: Newman HTML Extra Reporter

## Test Scenarios

The collection is organized into two main categories:

### 1) Positive Testing (Functional and Business Logic)

- Health Check: verify API status and availability.
- Checkout Workflow Simulation: create cart, add items, update quantities (Path Variables), and remove items.
- Authentication: register an API client to retrieve a Bearer token.
- Order Management: create and manage customer orders.

### 2) Negative Testing (Error Validation and Security)

- Authentication Validation: test missing required headers.
- Security Checks: validate invalid tokens and ensure 401 Unauthorized responses.
- Input Validation: test invalid inputs (invalid category values, exceeding max/min limits).

## How to Run Tests Locally

### Prerequisites

- Node.js installed (recommended: v18+)
- npm installed

### Steps

1. Clone the repository.

```bash
git clone https://github.com/adrian-raf/API-Test-using-Postman.git
```

2. Move into the project directory.

```bash
cd API-Test-using-Postman
```

3. Install Newman and HTML Extra Reporter globally.

```bash
npm install -g newman newman-reporter-htmlextra
```

4. Run the collection and generate CLI + HTML report.

```bash
newman run "Simple Grocery Store API.postman_collection.json" -r cli,htmlextra --reporter-htmlextra-export "newman/report.html"
```

### Test Output

- CLI result is shown directly in terminal.
- HTML report is generated at: newman/report.html

Open the HTML report in your browser to review detailed test results.
