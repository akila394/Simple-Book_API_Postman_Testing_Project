# Simple-Books API Postman Collection

This repository contains a Postman collection for testing and interacting with the **Simple-Books API**. The collection provides pre-configured requests to test the API endpoints for book management, such as viewing books, placing orders, and managing them.

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Collection Structure](#collection-structure)
- [Authorization](#authorization)
- [Using the Collection](#using-the-collection)
- [Global Variables](#global-variables)
- [Running the Collection via CLI](#running-the-collection-via-cli)
- [Contributing](#contributing)
- [License](#license)

## Overview
The Simple-Books API allows users to:
- Retrieve information about available books.
- Place, update, or delete book orders.
- Authenticate to access restricted endpoints.

This Postman collection simplifies interaction with the API by providing ready-to-use requests and tests.

## Prerequisites
- **Postman**: [Download here](https://www.postman.com/downloads/)
- Access to the [Simple-Books API documentation](https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md)

## Setup
1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Import the Postman collection:
   - Open Postman.
   - Click on **Import**.
   - Select the `Simple-Book API.postman_collection.json` file from this repository.

3. Set up the environment (optional):
   - Configure environment variables such as `baseUrl`, `AccessToken`, and any other required parameters.

## Collection Structure
Below is the structure of the collection:

### **Simple-Book API**
1. **GET API Status**: Check the API's health status.
2. **POST API Authentication**: Authenticate to access secure endpoints.
3. **GET List of Books**: Retrieve a list of available books.
4. **GET Get a Single Book**: Fetch details of a specific book by its ID.
5. **POST Order Books**: Place an order for a book.
6. **GET Get an Order**: Retrieve details of a specific order.
7. **GET Get all Orders**: Retrieve all orders placed by the user.
8. **PATCH Update Order**: Update an existing book order.
9. **DELETE Delete Order**: Delete a specific book order.

## Authorization
The API requires an API key for certain operations. To set up:
1. Obtain your API key from the API provider.
2. Set the `AccessToken` variable in the Postman environment or in the header of the requests.

## Using the Collection
1. Open Postman and select the imported collection.
2. Choose the desired request and click **Send**.
3. Edit parameters, headers, or body payload as required.

### Example: Placing an Order
- Select **POST Order Books**.
- Fill in the required fields (e.g., `book_id`, `customer_name`).
- Click **Send** to place the order.

## Global Variables
To use the provided global variables in this collection, follow these steps:

### Variables in Use
- **BaseUrl**: `https://simple-books-api.glitch.me`
- **AccessToken**: `eca2d422186e688a0d8cd1be...` (replace with your own token)
- **OrderID**: `bmhPXWeInHl4xwjV0Bh2...` (automatically set to Global variable when running the collection)

### Importing Global Variables
1. Open Postman.
2. Go to **Environments**.
3. Click **Import**.
4. Select the `workspace.postman_globals` file from this repository.

This will add the global variables to your Postman workspace. Make sure to update the variable values if needed.

## Running the Collection via CLI
To automate testing with the collection:
1. Install [Newman](https://www.npmjs.com/package/newman):
   ```bash
   npm install -g newman
   ```
2. Install the `newman-reporter-htmlextra` package for enhanced reporting:
   ```bash
   npm i newman-reporter-htmlextra
   ```
3. Run the collection using the following command:
   ```bash
   newman run "Simple-Book API.postman_collection.json" --globals "workspace.postman_globals.json"
   ```
4. Generate an HTML report using `newman-reporter-htmlextra`:
   ```bash
   newman run "Simple-Book API.postman_collection.json" --globals "workspace.postman_globals.json" --reporters cli,htmlextra
   ```

## Contributing
We welcome contributions to improve this collection! To contribute:
1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Submit a pull request.

---
For any questions or issues, please raise an issue in this repository or contact the maintainer.



