# Trip Expense Tracker API
This is a simple API for tracking trip expenses built with Node.js, Express and MongoDB.

## Overview
- Store trip names
- Log expenses for trips with fields for amount, category, date etc.
- GET trips and expenses
- MongoDB for data storage

## Usage
### Install

```
npm install
```


### Configure MongoDB
Update the MongoDB URL in index.js:

```
const url = "mongodb://localhost:27017"
```

### Run Server

```
node index.js
```

Server will run on port 3000.

## API Endpoints
POST /trip - Create a new trip
GET /trips - Get all trips
POST /expense - Create a new expense for a trip
GET /expenses - Get expenses for a trip
Trip and expense data is sent/received as JSON in the request body and response.

### Implementation
The main implementation files:

- index.js - Server setup and API route handlers
- MongoDB model functions in route handlers
- MongoDB is connected on app start and db/collections assigned to global variables for simple access in route handlers.

Error handling is done in each route by catching MongoDB errors and returning 500 status.

### Improvements
For a more robust implementation:

- Add validation for requests
- Use MongoDB models/schemas for better structure
- Handle connection errors properly
- Add user/authentication model
- Expand API functionality
Notes
This provides a very simple starting point for building an API with Node/Express/MongoDB. Many enhancements could be made for a real production API.
