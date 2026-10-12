# Smart Billing and Retailing System — Frontend

## Overview

The Smart Billing and Retailing System is a web-based application designed to simplify retail store operations. The frontend provides a user-friendly interface for managing products, customers, billing, inventory, and sales history.

The application connects with a Spring Boot backend to process data and store information in a MySQL database.

## Technologies Used

- React.js
- JavaScript
- HTML5
- CSS3
- Vite
- REST APIs
- Spring Boot (Backend)
- MySQL (Database)

## Features

### 1. Dashboard
- Displays an overview of retail store operations.
- Provides quick access to the main application modules.
- Presents key inventory and sales information when available.

### 2. Product Management
- Add new products.
- View available products.
- Update product details and prices.
- Manage product stock quantities.

### 3. Customer Management
- Add customer information.
- View customer records.
- Update customer details.

### 4. Billing Management
- Create customer bills.
- Add products to a bill.
- Calculate bill totals.
- Track purchased quantities and prices.

### 5. Sales History
- View previous sales records.
- Review billing information.
- Track completed transactions.

> Note: Available features depend on the current frontend implementation and its connection to the backend APIs.

## Project Structure

```text
Frontend/
├── public/
├── src/
│   ├── components/
│   ├── App.jsx
│   ├── App.css
│   ├── main.jsx
│   └── index.css
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

The exact structure may vary depending on the components created in the project.

## Prerequisites

Install the following before running the application:

- Node.js
- npm
- Google Chrome or another modern web browser
- Spring Boot backend
- MySQL Server

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/rupasric07-design/SmartBillingAndRetailing.git
```

### 2. Navigate to the Frontend Folder

```bash
cd SmartBillingAndRetailing/frontend
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Start the Development Server

```bash
npm run dev
```

### 5. Open the Application

Open the local URL displayed in the terminal, usually:

```text
http://localhost:5173
```

## Backend Integration

The frontend communicates with the Spring Boot backend through REST APIs.

Default backend address:

```text
http://localhost:8080
```

### API Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/products` | Retrieve products |
| POST | `/api/products` | Add a product |
| PUT | `/api/products/{id}` | Update a product |
| DELETE | `/api/products/{id}` | Delete a product |
| GET | `/api/customers` | Retrieve customers |
| POST | `/api/customers` | Add a customer |
| PUT | `/api/customers/{id}` | Update a customer |
| DELETE | `/api/customers/{id}` | Delete a customer |
| GET | `/api/billing` | Retrieve bills |
| POST | `/api/billing` | Create a bill |
| GET | `/api/sales` | Retrieve sales history |
| GET | `/api/sales/{id}` | Retrieve a sale by ID |

The frontend must use the corresponding backend endpoints for these operations to work with database records.

## Running the Complete Application

To run the complete system:

1. Start MySQL Server.
2. Configure the database connection in the backend.
3. Start the Spring Boot backend on port `8080`.
4. Open a terminal in the frontend directory.
5. Run `npm install` if dependencies are not installed.
6. Run `npm run dev`.
7. Open `http://localhost:5173` in your browser.

Keep both the backend and frontend running while testing integrated features.

## Future Enhancements

- User authentication and authorization.
- Improved inventory reporting.
- Low-stock notifications.
- Sales analytics and graphical reports.
- Invoice printing and PDF generation.
- Responsive design for mobile devices.

## Author

Developed as a Smart Billing and Retailing System project.

## License

This project is intended for educational and demonstration purposes.
