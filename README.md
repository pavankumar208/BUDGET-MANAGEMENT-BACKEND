# SmartSpend - Expense Tracker Backend

A comprehensive backend system for tracking personal finances, built with Node.js, Express, and MongoDB.

## Features

- User authentication with JWT
- Expense tracking and categorization
- Income management
- Budget planning and monitoring
- Reporting and analytics
- Dashboard with financial insights
- RESTful API design
- Input validation
- Documentation with Swagger

## API Documentation

API documentation is available at `/api-docs` when the server is running.

## Tech Stack

- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Express Validator for input validation
- Swagger for API documentation

## Installation

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env` file based on `.env.example`:
   ```
   cp .env.example .env
   ```
4. Update the `.env` file with your MongoDB URI and JWT secrets
5. Start the server:
   ```
   npm run dev
   ```

## API Endpoints

### Authentication
- POST `/api/auth/register` - Register a new user
- POST `/api/auth/login` - Login user
- POST `/api/auth/refresh` - Refresh access token
- POST `/api/auth/logout` - Logout user

### User
- GET `/api/user/profile` - Get current user profile
- PUT `/api/user/profile` - Update user profile
- PUT `/api/user/password` - Update user password
- PUT `/api/user/preferences` - Update user preferences

### Expenses
- GET `/api/expenses` - Get all expenses
- GET `/api/expenses/:id` - Get expense by ID
- POST `/api/expenses` - Create new expense
- PUT `/api/expenses/:id` - Update expense
- DELETE `/api/expenses/:id` - Delete expense

### Income
- GET `/api/income` - Get all income entries
- GET `/api/income/:id` - Get income by ID
- POST `/api/income` - Create new income entry
- PUT `/api/income/:id` - Update income entry
- DELETE `/api/income/:id` - Delete income entry

### Budget
- GET `/api/budget` - Get all budgets
- GET `/api/budget/:id` - Get budget by ID
- POST `/api/budget` - Create new budget
- PUT `/api/budget/:id` - Update budget
- DELETE `/api/budget/:id` - Delete budget
- GET `/api/budget/status/:month/:year` - Get budget status

### Reports
- GET `/api/report/monthly/:month/:year` - Get monthly expense report
- GET `/api/report/category-wise` - Get expense breakdown by category
- GET `/api/report/income-vs-expense` - Get income vs expense comparison
- GET `/api/report/trends` - Get expense trends over time

### Dashboard
- GET `/api/dashboard` - Get dashboard summary data

## Development

```
npm run dev
```

This starts the server in development mode with nodemon for automatic restarts when code changes.

## Testing

```
npm test
```

## License

MIT
