# MERN Stack Restaurant Reservation System

## Project Overview
The **MERN Stack Restaurant Reservation System** is a full-stack web application designed to streamline the process of managing restaurant reservations. This project leverages the **MERN stack** (MongoDB, Express.js, React.js, Node.js) to provide a robust and efficient solution for both customers and restaurant staff. The system includes features such as user authentication, reservation creation, and administrative controls, ensuring a seamless experience for all stakeholders.

---

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Future Enhancements](#future-enhancements)

---

## Features
### For Customers
- User registration and login.
- Browse available time slots.
- Create, update, and cancel reservations.

### For Restaurant Staff
- Dashboard to view and manage reservations.
- Update availability for time slots.
- Manage user accounts and permissions.

---

## Technologies Used

### Frontend
- **React.js**: For building the user interface.
- **Vite**: Development server and build tool.
- **CSS/SCSS**: Styling.
- **ESLint**: Code quality and linting.

### Backend
- **Node.js**: Server-side runtime.
- **Express.js**: Web framework.
- **MongoDB**: Database for storing reservation data.
- **Mongoose**: MongoDB object modeling.
- **Middleware**: Custom middleware for authentication and error handling.

### Deployment
- **Vercel**: Deployment for the backend.
- **Frontend Hosting**: Configured for modern web delivery.

---

## Project Structure

### Backend (`backend`)
- **`app.js`**: Initializes middleware and application logic.
- **`server.js`**: Entry point for the server.
- **`controller/`**: Contains business logic for reservations, users, and availability.
- **`database/`**: Configuration for MongoDB connection.
- **`middlewares/`**: Middleware functions for tasks like authentication.
- **`models/`**: Schema definitions for MongoDB collections.
- **`routes/`**: Defines API endpoints for user and reservation operations.
- **`vercel.json`**: Deployment configuration for Vercel.

### Frontend (`frontend`)
- **`src/`**: Main directory for React components and logic.
  - **`components/`**: Reusable UI components.
  - **`pages/`**: Page-level components (e.g., Home, Dashboard).
  - **`services/`**: API interaction logic.
- **`public/`**: Static assets like images and `index.html`.
- **`vite.config.js`**: Build tool configuration.
- **`.eslintrc.cjs`**: ESLint configuration for code quality.

---

## Installation

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- Git

### Steps
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd MERN_STACK_RESTAURANT_RESERVATION-main
   ```
2. Install dependencies for both backend and frontend:
   ```bash
   cd backend
   npm install
   cd ../frontend
   npm install
   ```
3. Set up environment variables:
   - Create a `.env` file in the `backend` directory with the following keys:
     ```env
     MONGO_URI=<your-mongodb-uri>
     PORT=5000
     JWT_SECRET=<your-jwt-secret>
     ```
4. Start the development servers:
   - Backend:
     ```bash
     cd backend
     npm start
     ```
   - Frontend:
     ```bash
     cd frontend
     npm run dev
     ```

---

## Usage
- Navigate to the frontend development server (default: `http://localhost:3000`).
- Use the interface to sign up, log in, and create reservations.
- Admins can log in to manage availability and monitor reservations.

---

## API Endpoints
### Users
- `POST /api/users/register`: Register a new user.
- `POST /api/users/login`: Authenticate a user.

### Reservations
- `GET /api/reservations`: Fetch all reservations.
- `POST /api/reservations`: Create a new reservation.
- `PUT /api/reservations/:id`: Update an existing reservation.
- `DELETE /api/reservations/:id`: Delete a reservation.

### Admin
- `GET /api/admin/dashboard`: Admin dashboard data.

---

## Future Enhancements
- Add support for multiple languages.
- Implement real-time notifications for reservation confirmations.
- Integrate third-party payment gateways.
- Enhance the admin dashboard with analytics and reporting.

---

## Contribution
Feel free to fork this repository and contribute by submitting pull requests. For major changes, please open an issue first to discuss what you would like to change.
