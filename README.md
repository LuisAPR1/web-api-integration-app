# Movies App

A full-stack web application for discovering and managing movies and TV shows. Built with React, TypeScript, and Node.js, this app provides users with a comprehensive platform to browse popular content, search for specific titles, manage favorites, and maintain user accounts.

## Features

### Frontend Features
- **Movie Discovery**: Browse popular, top-rated, now playing, and upcoming movies
- **TV Show Discovery**: Explore popular, top-rated, and currently airing TV shows
- **Advanced Search**: Search for movies and TV shows with real-time results
- **Movie Details**: View comprehensive information about movies including cast, crew, ratings, and reviews
- **Favorites System**: Save and manage your favorite movies and TV shows
- **User Authentication**: Secure user registration and login system
- **Account Management**: Edit user profile and account settings
- **Responsive Design**: Modern, mobile-friendly interface
- **Filter System**: Filter content by genre, certification, and year

### Backend Features
- **RESTful API**: Express.js server with TypeScript
- **User Authentication**: JWT-based authentication with bcrypt password hashing
- **Email Verification**: SMTP integration for account activation
- **Database**: NeDB for user data and favorites storage
- **Security**: Password hashing, JWT tokens, and input validation

## Tech Stack

### Frontend
- **React 18** - UI framework
- **TypeScript** - Type safety and development experience
- **React Router DOM** - Client-side routing
- **Axios** - HTTP client for API requests
- **Material-UI** - UI component library
- **Styled Components** - CSS-in-JS styling
- **React Icons** - Icon library

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **TypeScript** - Type safety
- **NeDB** - Embedded database
- **JWT** - Authentication tokens
- **bcrypt** - Password hashing
- **Nodemailer** - Email functionality
- **UUID** - Unique identifier generation

### External APIs
- **The Movie Database (TMDb)** - Movie and TV show data

## Project Structure

```
DAW/
├── client/                 # React frontend application
│   ├── public/            # Static assets
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Page components
│   │   ├── modules/       # API services and utilities
│   │   ├── context/       # React context providers
│   │   └── styles/        # CSS stylesheets
│   └── package.json
├── server/                # Node.js backend application
│   ├── src/
│   │   ├── types/         # TypeScript type definitions
│   │   ├── main.ts        # Express server setup
│   │   ├── users.ts       # User management logic
│   │   ├── SMTP.ts        # Email functionality
│   │   └── serverInfo.ts  # Server configuration
│   └── package.json
└── README.md
```

## Installation

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd DAW
   ```

2. **Install frontend dependencies**
   ```bash
   cd client
   npm install
   ```

3. **Install backend dependencies**
   ```bash
   cd ../server
   npm install
   ```

4. **Environment Setup**
   
   Create a `.env` file in the server directory with the following variables:
   ```env
   JWT_SECRET=your_jwt_secret_here
   SMTP_HOST=your_smtp_host
   SMTP_PORT=587
   SMTP_USER=your_email@example.com
   SMTP_PASS=your_email_password
   ```

## Running the Application

### Development Mode

1. **Start the backend server**
   ```bash
   cd server
   npm run dev
   ```
   The server will run on `http://localhost:8080`

2. **Start the frontend application**
   ```bash
   cd client
   npm start
   ```
   The application will open in your browser at `http://localhost:3000`

### Production Mode

1. **Build the frontend**
   ```bash
   cd client
   npm run build
   ```

2. **Start the backend**
   ```bash
   cd server
   npm run compile
   npm start
   ```

## API Endpoints

### Authentication
- `POST /register` - User registration
- `POST /login` - User login
- `GET /activate?token={token}` - Account activation

### User Management
- `GET /profile` - Get user profile (requires authentication)
- `PUT /profile` - Update user profile (requires authentication)
- `GET /favorites` - Get user favorites (requires authentication)
- `POST /favorites` - Add to favorites (requires authentication)
- `DELETE /favorites/:id` - Remove from favorites (requires authentication)

## Usage

1. **Browse Movies**: Visit the home page to see popular, top-rated, and upcoming movies
2. **Search Content**: Use the search bar to find specific movies or TV shows
3. **View Details**: Click on any movie or TV show to see detailed information
4. **Create Account**: Register for an account to access personalized features
5. **Manage Favorites**: Add movies and TV shows to your favorites list
6. **Filter Content**: Use the filter bar to narrow down results by genre, year, or rating

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.

## Acknowledgments

- [The Movie Database (TMDb)](https://www.themoviedb.org/) for providing the movie and TV show data API
- React and TypeScript communities for excellent documentation and tools

---

*This README was AI generated by Claude 2.7 Sonnet*
