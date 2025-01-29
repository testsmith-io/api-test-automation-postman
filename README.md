# API Test Automation with Postman (and Newman)

[![API Test Automation with Postman and Newman - Run Tests](https://github.com/testsmith-io/api-test-automation-postman/actions/workflows/postman.yml/badge.svg)](https://github.com/testsmith-io/api-test-automation-postman/actions/workflows/postman.yml)

This repository contains example collections and scripts for API test automation using:
- **Postman** for API request management and testing.
- **Newman** for running Postman collections via the command line.

## Features
- Examples of GET, POST, and Protected API requests.
- Comprehensive demonstration of API testing workflows with assertions and pre/post-request scripts.
- Fully automated CI pipeline using GitHub Actions to run Postman collections.

## Test API
All examples in this repository are designed to work with the **Practice Software Testing API**, a publicly available API for learning and practicing software testing. You can explore the API documentation and endpoints here:  
👉 **[Practice Software Testing API](https://api.practicesoftwaretesting.com/api/documentation)** 👈

## Examples Included
1. **GET Request**: Fetch a list of brands with `GET /brands`.
2. **Login API**: Authenticate using `POST /login` with an email/password payload.
3. **Protected API Request**: Authenticate, then use a token to fetch data with `GET /invoices`.

## Prerequisites
- **Postman** installed locally (or a web account for Postman Cloud).
- **Newman**, the Postman command-line tool. Install it globally with:
  ```bash
  npm install -g newman
  ```
- **newman-reporter-htmlextra**, a Newman HTML reporter. Install it globally with:
  ```bash
  npm install -g newman-reporter-htmlextra
  ```

## Setup and Run
1. Clone this repository:
   ```bash
   git clone https://github.com/testsmith-io/api-test-automation-postman.git
   ```
2. Navigate to the project directory:
   ```bash
   cd api-test-automation-postman
   ```
3. Run the Postman collection using Newman:
   ```bash
   newman run collections/example-collection.json -r htmlextra
   ```

## Automated Workflow
The repository includes a GitHub Actions workflow to automatically execute the Postman collections with Newman. It runs on every `push` and `pull_request` to ensure the tests pass seamlessly.