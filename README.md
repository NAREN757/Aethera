# Aethera — Stay & Property Listing Platform

Aethera is a full-stack web application that allows users to explore property listings, create accounts, manage their own listings, and share reviews. Built using Node.js, Express.js, MongoDB, and EJS, the project focuses on server-side development, authentication, session management, and CRUD operations.

**Live Demo:** [Aethera](https://aethera-2yx3.onrender.com)

---

## Features

- **User Authentication:** User registration, login, and logout using Passport.js and local authentication.
- **Property Listings:** Browse available properties and view individual listing details.
- **Listing Management:** Create, edit, and delete property listings.
- **Review System:** Add and manage reviews for property listings.
- **Authorization:** Restrict listing and review modifications to authorized users.
- **Session Management:** Maintain authenticated sessions using Express Session and MongoDB.
- **Form Validation:** Validate submitted data on the server using Joi.
- **Flash Messages:** Display success and error messages for user actions.
- **Responsive UI:** Build a clean interface using EJS templates, Bootstrap, and custom CSS.
- **Cloud Deployment:** Deploy the application on Render with MongoDB Atlas as the database.

## Tech Stack

| Category | Technologies |
|---|---|
| Frontend | HTML5, CSS3, JavaScript, Bootstrap |
| Templating | EJS, EJS-Mate |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Authentication | Passport.js, Passport Local, Passport Local Mongoose |
| Sessions | Express Session, Connect-Mongo |
| Validation | Joi |
| Middleware | Method Override, Connect Flash |
| Deployment | Render |

## Technical Implementation

### 1. Authentication and Session Management
Implemented user authentication using Passport Local and Passport Local Mongoose. Express Session maintains user sessions, while Connect-Mongo stores session data in MongoDB.

### 2. CRUD Operations
Implemented Create, Read, Update, and Delete operations for property listings and reviews using Express routes and Mongoose models.

### 3. Authorization Middleware
Created reusable middleware to verify login status, listing ownership, and review authorship before allowing protected operations.

### 4. Server-Side Validation
Used Joi schemas to validate incoming listing and review data before saving it to the database.

### 5. RESTful Routing
Organized application endpoints into separate Express routers for users, listings, and reviews, improving code organization and maintainability.

### 6. Error Handling
Used reusable asynchronous error-handling middleware and a centralized Express error handler to manage application errors.

### 7. Production Deployment
Configured environment variables for database connectivity and session security, and configured Express to trust Render's reverse proxy for secure session cookies.

## Project Structure

```text
Aethera/
├── controllers/
│   ├── listings.js
│   ├── reviews.js
│   └── users.js
├── models/
│   ├── listing.js
│   ├── review.js
│   └── user.js
├── routes/
│   ├── listing.js
│   ├── review.js
│   └── user.js
├── middleware.js
├── utils/
│   ├── ExpressError.js
│   └── wrapAsync.js
├── views/
│   ├── layouts/
│   ├── listings/
│   ├── users/
│   └── error.ejs
├── public/
│   ├── css/
│   └── js/
├── schema.js
├── app.js
├── package.json
└── README.md
```

## Installation and Setup

### Prerequisites
- Node.js and npm
- MongoDB database or MongoDB Atlas account
- Git

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
cd Aethera
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the project root:

```env
ATLASDB_URL=your_mongodb_connection_string
SESSION_SECRET=your_session_secret
NODE_ENV=development
```

Never commit your `.env` file or expose database credentials.

### 4. Start the Application

Use the start command configured in your `package.json`. If no start script exists, you can run:

```bash
node app.js
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Environment Configuration

For production deployment, configure `ATLASDB_URL`, `SESSION_SECRET`, and `NODE_ENV=production` in the Render environment settings.

## What I Learned

- Building a full-stack web application using the MVC architecture.
- Designing RESTful routes and implementing CRUD operations.
- Implementing authentication and authorization with Passport.js.
- Managing persistent user sessions using MongoDB.
- Validating data and handling errors in Express applications.
- Deploying a Node.js application and configuring production environment variables.
- Debugging deployment and browser-specific issues.

## Future Improvements

- Property search, filtering, and sorting.
- Image uploads through cloud storage.
- Maps and location-based property discovery.
- Pagination and improved listing performance.
- Automated testing and CI/CD integration.

## Author

**Narendra Giriyappanavar**

GitHub: [NAREN757](https://github.com/NAREN757)

Portfolio: [View Portfolio](https://naren757.github.io/Portfolio/)

---

*Built as a full-stack web development project to practice backend engineering, database integration, authentication, and deployment.*
