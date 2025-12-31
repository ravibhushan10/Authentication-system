# 🔐 MERN Authentication System

A modern, secure full-stack authentication system built with the MERN stack. Features include user registration, login, profile management, and JWT-based authentication with HTTP-only cookies.

## 📸 Screenshots
<table align="center">
  <tr>
    <td align="center">
      <img src="screenshots/home.png" ><br/>
      <em>Home Page</em>
    </td>
    <td align="center">
      <img src="screenshots/login.png" ><br/>
      <em>Login Screen</em>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="screenshots/register.png" ><br/>
      <em>Registration Screen</em>
    </td>
    <td align="center">
      <img src="screenshots/profile.png"><br/>
      <em>Profile Management</em>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="screenshots/dashboard.png" ><br/>
      <em>User Dashboard</em>
    </td>
     <td align="center">
      <img src="screenshots/navbar.png" ><br/>
      <em>Navigation Bar</em>
    </td>
  </tr>
</table>


## [Live Demo](#)

## 🌟 Features

### 🎨 **Modern UI/UX**
- Beautiful gradient design with purple theme
- Glassmorphism effects and shadows
- Smooth animations and hover effects
- Fully responsive design for all devices
- Eye icons for password visibility toggle
- Professional navigation with user dropdown

### 🔐 **Authentication & Security**
- User registration with validation
- Secure login system
- JWT-based authentication
- HTTP-only cookies for token storage
- Password hashing with bcrypt
- Protected routes and middleware
- Logout functionality

### 👤 **User Management**
- User profile page
- Update name and password
- Email displayed (non-editable for security)
- Password confirmation validation
- Real-time form validation
- Toast notifications for user feedback

### 🛡️ **Security Features**
- Password strength requirements
- HTTP-only cookie implementation
- JWT token expiration
- Protected API routes
- CORS configuration for production
- Environment variable management
- Error handling middleware

### 🚀 **Technical Excellence**
- Redux Toolkit for state management
- RTK Query for API calls
- React Bootstrap for UI components
- React Icons for modern iconography
- MongoDB for database
- Express.js RESTful API
- Production-ready deployment configuration

## 🛠️ Technologies Used

### Frontend (Client)
| Technology | Purpose | Version |
|------------|---------|---------|
| React | UI Framework | 18+ |
| Redux Toolkit | State Management | Latest |
| RTK Query | Data Fetching | Latest |
| React Router | Navigation | Latest |
| React Bootstrap | UI Components | Latest |
| React Icons | Icon Library | Latest |
| React Toastify | Notifications | Latest |
| Vite | Build Tool | Latest |

### Backend (Server)
| Technology | Purpose | Version |
|------------|---------|---------|
| Node.js | Runtime Environment | 16+ |
| Express.js | Web Framework | Latest |
| MongoDB | Database | Latest |
| Mongoose | ODM | Latest |
| JWT | Authentication | Latest |
| bcryptjs | Password Hashing | Latest |
| cookie-parser | Cookie Management | Latest |
| cors | Cross-Origin Requests | Latest |

### DevOps & Tools
| Tool | Purpose |
|------|---------|
| Git | Version Control |
| npm | Package Management |
| Postman | API Testing |
| dotenv | Environment Variables |

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or Atlas)
- npm or yarn package manager

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/mern-auth.git
   cd mern-auth
   ```

2. **Install Client Dependencies**
   ```bash
   cd client
   npm install
   ```

3. **Install Server Dependencies**
   ```bash
   cd ../server
   npm install
   ```

4. **Client Environment Variables: Create `.env` file in `client/` root directory**
   ```env
   # For Development
   REACT_APP_API_URL=http://localhost:5000

   # For Production (update when deploying)
   # REACT_APP_API_URL=https://your-backend-domain.com
   ```

5. **Server Environment Variables: Create `.env` file in `server/` root directory**
   ```env
   # Server Configuration
   PORT=5000
   NODE_ENV=development

   # Database
   MONGO_URI=your_mongodb_connection_string

   # JWT Secret (use a strong random string)
   JWT_SECRET=your_super_secret_jwt_key_here

   # Frontend URL for CORS
   CLIENT_URL=http://localhost:3000

   # For Production
   # CLIENT_URL=https://your-frontend-domain.com
   ```

6. **Start the Server**
   ```bash
   cd server
   npm start
   # Server will run on http://localhost:5000
   ```

7. **Start the Client** (in a new terminal)
   ```bash
   cd client
   npm start
   # Client will run on http://localhost:3000
   ```

## 📖 Usage Guide

### For Users

1. **Register an Account**
   - Navigate to the Register page
   - Fill in your name, email, and password
   - Confirm your password
   - Click "Register" to create your account

2. **Login**
   - Navigate to the Login page
   - Enter your email and password
   - Click "Sign In" to access your account

3. **Profile Management**
   - Click on your name in the navigation bar
   - Select "Profile" from the dropdown
   - Update your name or password
   - Email is displayed but cannot be changed (for security)
   - Leave password fields blank if you don't want to change it

4. **Logout**
   - Click on your name in the navigation bar
   - Select "Logout" from the dropdown
   - You'll be redirected to the login page

### For Developers

1. **API Endpoints**
   - `POST /api/users/register` - Register new user
   - `POST /api/users/login` - Login user
   - `POST /api/users/logout` - Logout user
   - `GET /api/users/profile` - Get user profile (protected)
   - `PUT /api/users/profile` - Update user profile (protected)

2. **Protected Routes**
   - Routes are protected using JWT middleware
   - Only authenticated users can access protected endpoints
   - Frontend uses PrivateRoute component for route protection

3. **State Management**
   - Redux store manages authentication state
   - User info stored in Redux and localStorage
   - RTK Query handles API calls and caching

## 🔒 Security Best Practices

### Implemented Security Measures
- ✅ Passwords hashed with bcrypt (10 salt rounds)
- ✅ JWT tokens stored in HTTP-only cookies
- ✅ CORS configured for production deployment
- ✅ Environment variables for sensitive data
- ✅ Protected API routes with authentication middleware
- ✅ Input validation on frontend and backend
- ✅ Email used as unique identifier (cannot be changed)
- ✅ Password confirmation on registration and updates

### Additional Recommendations
- Use strong JWT secret in production
- Enable rate limiting on API endpoints
- Implement account lockout after failed login attempts
- Add email verification for new registrations
- Set up HTTPS in production
- Regular security audits and updates

## 📁 Project Structure

```
mern-auth/
├── client/                 # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   │   ├── FormContainer.jsx
│   │   │   ├── Header.jsx
│   │   │   ├── Hero.jsx
│   │   │   ├── Loader.jsx
│   │   │   └── PrivateRoute.jsx
│   │   ├── screens/       # Page components
│   │   │   ├── HomeScreen.jsx
│   │   │   ├── LoginScreen.jsx
│   │   │   ├── RegisterScreen.jsx
│   │   │   └── ProfileScreen.jsx
│   │   ├── slices/        # Redux slices
│   │   │   ├── authSlice.js
│   │   │   ├── usersApiSlice.js
│   │   │   └── apiSlice.js
│   │   ├── store.js       # Redux store
│   │   ├── App.js
│   │   └── index.js
│   ├── .env
│   └── package.json
│
├── server/                # Node.js backend
│   ├── config/
│   │   └── db.js         # MongoDB connection
│   ├── controllers/
│   │   └── userController.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── errorMiddleware.js
│   ├── models/
│   │   └── userModel.js
│   ├── routes/
│   │   └── userRoutes.js
│   ├── utils/
│   │   └── generateToken.js
│   ├── .env
│   ├── index.js
│   └── package.json
│
└── README.md
```

## 🚀 Deployment

### Frontend Deployment (Vercel/Netlify)

1. **Build the client**
   ```bash
   cd client
   npm run build
   ```

2. **Deploy to Vercel**
   ```bash
   vercel deploy --prod
   ```

3. **Set Environment Variables**
   - Add `REACT_APP_API_URL` with your backend URL

### Backend Deployment (Render/Railway/Heroku)

1. **Prepare for deployment**
   - Ensure all dependencies are in `package.json`
   - Set `NODE_ENV=production`

2. **Set Environment Variables**
   - `PORT`
   - `MONGO_URI`
   - `JWT_SECRET`
   - `CLIENT_URL` (your frontend URL)

3. **Deploy**
   - Push to GitHub
   - Connect to deployment platform
   - Deploy from main branch

### Post-Deployment

1. **Update CORS origins**
   ```javascript
   app.use(cors({
     origin: process.env.CLIENT_URL,
     credentials: true
   }));
   ```

2. **Update API URL in frontend**
   - Set `REACT_APP_API_URL` to production backend URL

3. **Test all features**
   - Registration
   - Login
   - Profile updates
   - Logout

## 🤝 Contributing

### How to Contribute

1. **Fork the Repository**
   - Click the 'Fork' button at the top right of this repository
   - This creates a copy of the project in your GitHub account

2. **Clone Your Fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/mern-auth.git
   cd mern-auth
   ```

3. **Create a Branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

4. **Make Your Changes**
   - Write clean, readable code
   - Follow the existing code style
   - Test your changes thoroughly
   - Update documentation if needed

5. **Commit Your Changes**
   ```bash
   git add .
   git commit -m 'Add some AmazingFeature'
   ```

6. **Push to Your Fork**
   ```bash
   git push origin feature/AmazingFeature
   ```

7. **Open a Pull Request**
   - Go to your forked repository on GitHub
   - Click **"Compare & pull request"**
   - Fill in the PR form:
     - **Title**: Brief summary (e.g., "Add password strength indicator")
     - **Description**: Explain your changes clearly:
       - What changes you made
       - Why you made them
       - Screenshots (if UI changes)
       - Related issue numbers (e.g., "Fixes #123")
   - Click **"Create pull request"**
   - Wait for review and be responsive to feedback

### Contribution Ideas
- Add email verification
- Implement forgot password functionality
- Add social authentication (Google, GitHub)
- Create user roles and permissions
- Add two-factor authentication
- Improve UI/UX with more animations
- Add dark/light theme toggle
- Create admin dashboard

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author
**Your Name**
- LinkedIn: [Your LinkedIn Profile](#)
- Portfolio: [Your Portfolio Website](#)
- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com

## 🙏 Acknowledgments

- React Bootstrap for the UI components
- MongoDB team for the excellent database
- Express.js community for the robust framework
- Redux Toolkit for simplified state management

---
<div align="center">
   
### ⭐ Star this repository if it helped you!
**Made with ❤️ by Your Name**
   
   
[Live Demo](#) · [Report Bug](https://github.com/yourusername/mern-auth/issues) · [Request Feature](https://github.com/yourusername/mern-auth/issues)

</div>

---
