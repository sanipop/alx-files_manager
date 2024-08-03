# Project ReadMe

## Files Manager Platform

### Overview
This project is designed to build a simple platform to upload and view files, integrating various backend technologies and techniques learned throughout the trimester. The platform provides functionalities for user authentication, file management, and background processing. The project incorporates the use of Node.js, Express, MongoDB, Redis, and other modern backend tools.

### Features
1. **User Authentication**
   - Users can authenticate using tokens.
   - Secure authentication through hashed passwords and token-based sessions.

2. **File Management**
   - List all files associated with a user.
   - Upload new files with support for different types (folder, file, image).
   - Change file permissions (public/private).
   - View file details and contents.
   - Generate thumbnails for image files.

3. **Background Processing**
   - Utilize Redis for managing temporary data and background tasks.
   - Background worker setup for handling tasks like generating thumbnails.

### Technology Stack
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Caching**: Redis
- **Task Queue**: Kue
- **Other Tools**: ES6, Mocha, Nodemon, Bull, Image Thumbnail, Mime-Types

### Project Structure
- **utils/redis.js**: Redis utility functions for caching and data retrieval.
- **utils/db.js**: MongoDB utility functions for database operations.
- **server.js**: Main server file setting up Express and routes.
- **routes/index.js**: Route definitions for various endpoints.
- **controllers/**: Contains the logic for handling API requests.

### Setup and Installation
1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/alx-files_manager.git
   cd alx-files_manager
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Environment Variables**
   - Set the necessary environment variables for MongoDB and Redis connections in a `.env` file:
     ```bash
     DB_HOST=localhost
     DB_PORT=27017
     DB_DATABASE=files_manager
     REDIS_HOST=localhost
     REDIS_PORT=6379
     ```

4. **Start the Server**
   ```bash
   npm run dev
   ```

### Usage
- **User Operations**:
  - Create a new user.
  - Authenticate a user and generate a token.
  - Get user details based on the token.

- **File Operations**:
  - Upload files and folders.
  - List files with pagination.
  - View file details.
  - Change file permissions.

### Endpoints
- **User Endpoints**:
  - `POST /users`: Create a new user.
  - `GET /connect`: Authenticate a user.
  - `GET /disconnect`: Sign out a user.
  - `GET /users/me`: Get authenticated user details.

- **File Endpoints**:
  - `POST /files`: Upload a new file.
  - `GET /files/:id`: Get file details.
  - `GET /files`: List files with optional parent ID and pagination.

### Learning Objectives
- Create an API with Express.
- Authenticate users securely.
- Store data in MongoDB.
- Utilize Redis for caching and background tasks.
- Implement background processing with Kue.

### Requirements
- **Editors**: vi, vim, emacs, Visual Studio Code.
- **Environment**: Ubuntu 18.04 LTS, Node.js 12.x.x.
- **Linting**: ESLint.

### Provided Files
- `package.json`
- `.eslintrc.js`
- `babel.config.js`

### Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any improvements or fixes.

### License
This project is licensed under the MIT License.

Enjoy building your Files Manager Platform!
