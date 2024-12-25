# ProjectHub Application (MERN Stack)

## Overview
The **ProjectHub Application** is a collaborative platform built using the MERN stack (MongoDB, Express.js, React.js, Node.js). It allows users to create, share, and manage projects while collaborating with team members in real-time.

## Features

- **User Authentication**: Secure sign-up and login using email and password.
- **Project Management**: Create, update, and delete projects.
- **Task Assignment**: Assign tasks to team members and track progress.
- **Team Collaboration**: Invite team members to collaborate on projects.
- **Real-time Updates**: Get instant updates on project changes.
- **Dashboard**: View all projects and their statuses at a glance.
- **Search and Filter**: Easily search for projects and filter by category, status, or team members.

## Tech Stack

- **Frontend**: React.js, Redux (for state management)
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Token)
- **Styling**: Tailwind CSS

## Installation

### Prerequisites
Ensure you have the following installed on your system:
- Node.js (v14 or higher)
- MongoDB (local or cloud-based, e.g., MongoDB Atlas)

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/projecthub.git
   cd projecthub
   ```

2. **Install Dependencies**:
   Navigate to both the `client` and `server` directories to install dependencies:
   ```bash
   cd client
   npm install
   cd ../server
   npm install
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the `server` directory with the following keys:
   ```env
   PORT=5000
   MONGO_URI=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret
   ```

4. **Run the Application**:
   - Start the backend server:
     ```bash
     cd server
     npm start
     ```
   - Start the frontend client:
     ```bash
     cd client
     npm start
     ```

5. **Access the App**:
   Open your browser and navigate to `http://localhost:3000`.

## Folder Structure

```
projecthub/
│
├── client/                # Frontend code
│   ├── public/            # Static files
│   ├── src/               # React app source code
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Pages for the app
│   │   ├── redux/         # Redux setup
│   │   └── App.js         # Root component
│
├── server/                # Backend code
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── controllers/       # Route handlers
│   └── server.js          # Entry point
│
└── README.md              # Documentation
```

## API Endpoints

### User Authentication
- **POST /api/auth/register**: Register a new user
- **POST /api/auth/login**: Log in an existing user

### Projects
- **POST /api/projects**: Create a new project
- **GET /api/projects**: Fetch all projects
- **GET /api/projects/:id**: Fetch a specific project
- **PUT /api/projects/:id**: Update project details
- **DELETE /api/projects/:id**: Delete a project

### Tasks
- **POST /api/projects/:id/tasks**: Add a task to a project
- **PUT /api/tasks/:id**: Update task details
- **DELETE /api/tasks/:id**: Delete a task

### Collaboration
- **POST /api/projects/:id/invite**: Invite a team member to a project

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes.
4. Push to the branch.
5. Submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgements
- Open-source libraries and tools that made this project possible.
- Inspiration from modern project management applications.
