# Nest_Ecommerce

https://github.com/Rakibulislam-emon/nest_client 

https://github.com/Rakibulislam-emon/nest_server

https://nest-client-henna.vercel.app/


# Nest Grocery Shop

A full-stack e-commerce platform for organic groceries with a React frontend and Express backend.

![Nest Logo](./nest_client/src/assets/logo.png)

## Project Overview

Nest Grocery Shop is a modern e-commerce application that provides a seamless shopping experience for organic grocery products. The project consists of two main parts:

1. **Nest Client** - Frontend built with React, Vite, and Tailwind CSS
2. **Nest Server** - Backend API built with Express.js and MongoDB

## Features

- 🛒 Complete e-commerce functionality
- 🔐 User authentication with Clerk
- 💳 Secure payment processing with Stripe
- 📱 Responsive design for all devices
- 🔍 Advanced product search and filtering
- 📊 Featured categories and popular products
- 📦 Shopping cart with Redux Persist
- 💰 Special deals and promotions

## Tech Stack

### Frontend (Nest Client)
- **Framework**: React 18, Vite
- **Styling**: Tailwind CSS
- **State Management**: Redux Toolkit with Redux Persist
- **Data Fetching**: TanStack React Query
- **Authentication**: Clerk
- **Payment Processing**: Stripe
- **Routing**: React Router
- **Notifications**: React Hot Toast
- **UI Components**: Headless UI, React Icons, Swiper

### Backend (Nest Server)
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB
- **Payment Processing**: Stripe
- **Authentication**: JWT
- **Date Handling**: Moment.js
- **HTTP Client**: Axios
- **Security**: bcrypt for password hashing
- **Environment Variables**: dotenv

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- MongoDB instance (local or Atlas)
- npm or yarn
- Stripe account for payment processing
- Clerk account for authentication

### Installation and Setup

#### 1. Clone the repository
```bash
git clone https://github.com/yourusername/nest-grocery-shop.git
cd nest-grocery-shop
```

#### 2. Set up the Backend (Nest Server)
```bash
cd nest_server
npm install

# Create .env file with the following variables
# PORT=5000
# URI=your_mongodb_connection_string
# STRIPE_KEY=your_stripe_secret_key
# JWT_SECRET=your_jwt_secret

# Start the development server
npm run dev
```

#### 3. Set up the Frontend (Nest Client)
```bash
cd ../nest_client
npm install

# Create .env file with the following variables
# VITE_API_URL=http://localhost:5000
# VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key

# Start the development server
npm run dev
```

#### 4. Access the application
- Frontend: http://localhost:5173
- Backend API: http://localhost:5000

## Project Structure

```
nest-grocery-shop/
├── nest_client/           # Frontend application
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── hooks/
│   │   ├── pages/
│   │   ├── providers/
│   │   ├── redux/
│   │   ├── routes/
│   │   ├── main.jsx
│   │   └── index.css
│   ├── .env
│   ├── index.html
│   ├── package.json
│   ├── tailwind.config.js
│   └── vite.config.js
│
├── nest_server/           # Backend application
│   ├── config/
│   ├── helper/
│   ├── routes/
│   │   ├── Authentication/
│   │   ├── payment/
│   │   └── ...
│   ├── .env
│   ├── index.js
│   ├── package.json
│   └── vercel.json
│
└── README.md
```

## API Endpoints

### Products
- `GET /api/products` - Get all products with filtering, sorting, and pagination
- `GET /api/product-details/:id` - Get product details by ID
- `GET /api/products/featured-categories` - Get featured product categories
- `GET /api/popular-products` - Get popular products (rating > 4.7)
- `GET /api/deals` - Get current deals and promotions

### Authentication
- `POST /api/register` - Register a new user

### Payment
- `POST /api/payment/process` - Process payment with Stripe

## Deployment

Both the client and server are configured for deployment on Vercel:

- **Frontend**: The `vercel.json` file in the client directory includes the necessary rewrites for client-side routing.
- **Backend**: The `vercel.json` file in the server directory includes the necessary configuration for serverless deployment.

## CORS Configuration

The server is configured to accept requests from:
- `https://nest-client-henna.vercel.app`
- `http://localhost:5173` (for local development)

## License

[MIT](LICENSE)

## Acknowledgements

- [React](https://reactjs.org/)
- [Vite](https://vitejs.dev/)
- [Express.js](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Redux Toolkit](https://redux-toolkit.js.org/)
- [React Query](https://tanstack.com/query/latest)
- [Clerk](https://clerk.dev/)
- [Stripe](https://stripe.com/)
