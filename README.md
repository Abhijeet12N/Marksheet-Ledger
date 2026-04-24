# College Marksheet Management System 🚀

An advanced, secure, and efficient web application designed for educational institutions to manage student academic records. This full-stack project features a modern React frontend and a robust Node.js backend, focusing on a smart, automated workflow for teachers to reduce errors and save time.

---

## Key Features ✨

- **Secure Teacher Authentication**: Implements JWT (JSON Web Tokens) with a secure `httpOnly` refresh token in a cookie to persist user sessions and protect against XSS attacks.
- **Student Information System (SIS)**: Full CRUD (Create, Read, Update, Delete) functionality for student records.
- **Intelligent Result Management**:
  - A "smart" workflow that automatically determines the correct academic year and semester for result entry based on the student's admission details.
  - Dynamic subject population based on the student's year, department, and a special grouping logic for the first year.
  - Handles complex evaluation schemes (ISE, MSE, ESE).
- **Dynamic Data Model**: The system is built around a "single source of truth" model where a student's current academic year is calculated dynamically, eliminating the need for manual annual updates.
- **Role-Based Authorization**: A security layer that prevents teachers from accessing or modifying records of students from other departments.
- **Analytics Dashboard**: Provides a comprehensive overview of key statistics, including pass percentages, department-wise performance, and recent activities.
- **Efficient & Modern Frontend**:
  - Built with React and TypeScript.
  - Utilizes lazy loading for faster initial page loads.
  - Features an optimized routing structure that prevents unnecessary re-rendering of layout components.

---

## Tech Stack ⚙️

### Frontend

- **React.js**: For building the user interface.
- **TypeScript**: For static typing and improved developer experience.
- **Vite**: Next-generation frontend tooling for a fast development experience.
- **Tailwind CSS**: A utility-first CSS framework for rapid UI development.
- **React Router**: For client-side routing.
- **Fetch API**: For making requests to the backend.

### Backend

- **Node.js**: JavaScript runtime for the server.
- **Express.js**: A minimal and flexible Node.js web application framework.
- **MongoDB**: NoSQL database for storing application data.
- **Mongoose**: An Object Data Modeling (ODM) library for MongoDB and Node.js.
- **JSON Web Token (JWT)**: For handling secure authentication.
- **Bcrypt.js**: For hashing user passwords.

---

## Getting Started 🚦

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or Atlas cloud)
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   JWT_REFRESH_SECRET=your_refresh_token_secret
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

   This will start both the frontend (Vite) and backend (Express) servers concurrently.

---

## Project Structure 📂

```
marksheet-ledger/
├── server/                 # Backend
│   ├── controllers/        # Route handlers
│   ├── data/               # Static data files
│   ├── middleware/         # Custom middleware
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── utils/             # Utility functions
│   └── index.js            # Server entry point
├── src/                    # Frontend
│   ├── components/         # React components
│   ├── context/           # React context providers
│   ├── helpers/           # Helper functions & types
│   ├── pages/             # Page components
│   ├── App.tsx            # Main app component
│   └── main.tsx           # React entry point
├── package.json
├── vite.config.ts
└── tailwind.config.js
```

---

## Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start both frontend and backend in development mode |
| `npm run client` | Start only the frontend (Vite) |
| `npm run server` | Start only the backend (Express with nodemon) |
| `npm run build` | Build the frontend for production |
| `npm run preview` | Preview the production build |
| `npm run lint` | Run ESLint |

---

## License 📄

This project is licensed under the MIT License.
