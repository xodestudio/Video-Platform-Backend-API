# Video Platform Backend API

## Project Overview

This project is a robust and scalable backend API for a video platform, designed to handle user authentication, video uploads, and other core functionalities. It provides a solid foundation for building a comprehensive video-sharing application, focusing on efficient data management, secure authentication, and seamless integration with cloud storage services.

## Features

- **User Authentication & Authorization:** Secure user registration, login, and access control using JSON Web Tokens (JWT).
- **Video Management:** API endpoints for uploading, managing, and retrieving video content.
- **Cloud Storage Integration:** Seamless integration with Cloudinary for efficient and scalable cloud-based video and image uploads.
- **Database Management:** Utilizes MongoDB for flexible and scalable data storage, with Mongoose for object data modeling.
- **Middleware & Error Handling:** Robust middleware for request processing, authentication, and centralized error handling.
- **CORS Enabled:** Configured for Cross-Origin Resource Sharing to allow frontend applications to interact with the API.

## Technologies Used

- **Backend:**
  - Node.js: JavaScript runtime environment.
  - Express.js: Fast, unopinionated, minimalist web framework for Node.js.
  - MongoDB: NoSQL database for flexible data storage.
  - Mongoose: MongoDB object data modeling (ODM) for Node.js.
  - JWT (jsonwebtoken): For secure authentication and authorization.
  - Bcrypt: For hashing passwords securely.
  - Multer: Node.js middleware for handling `multipart/form-data`, primarily used for uploading files.
  - Cloudinary: Cloud-based image and video management service.
  - Cors: Node.js package for providing a Connect/Express middleware that can be used to enable CORS with various options.
  - Cookie-parser: Parse Cookie header and populate `req.cookies` with an object keyed by the cookie names.
  - Dotenv: Loads environment variables from a `.env` file.
- **Development Tools:**
  - Nodemon: A tool that helps develop Node.js based applications by automatically restarting the node application when file changes in the directory are detected.
  - Prettier: An opinionated code formatter.

## Installation

To set up the project locally, follow these steps:

1.  **Clone the repository:**

    ```bash
    git clone <repository-url>
    cd video-platform-backend-api
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Configure Environment Variables:**

    - Create a `.env` file in the root of your project.
    - Copy the content from `.env.sample` into your new `.env` file.
    - Update the placeholder values with your actual credentials and configurations:

      ```
      PORT=8000
      MONGODB_URI="YOUR_MONGODB_CONNECTION_STRING"
      CORS_ORIGIN="*" # Or your frontend URL, e.g., http://localhost:3000
      ACCESS_TOKEN_SECRET="YOUR_ACCESS_TOKEN_SECRET"
      ACCESS_TOKEN_EXPIRY="1d"
      REFRESH_TOKEN_SECRET="YOUR_REFRESH_TOKEN_SECRET"
      REFRESH_TOKEN_EXPIRY="10d"
      CLOUDINARY_CLOUD_NAME="YOUR_CLOUDINARY_CLOUD_NAME"
      CLOUDINARY_API_KEY="YOUR_CLOUDINARY_API_KEY"
      CLOUDINARY_API_SECRET="YOUR_CLOUDINARY_API_SECRET"
      ```

      - **MONGODB_URI:** Your MongoDB connection string (e.g., from MongoDB Atlas).
      - **CORS_ORIGIN:** The origin(s) allowed to access your API. Use `*` for development, but specify your frontend URL(s) in production.
      - **ACCESS_TOKEN_SECRET & REFRESH_TOKEN_SECRET:** Strong, random strings for JWT secrets. You can generate these online.
      - **CLOUDINARY_CLOUD_NAME, CLOUDINARY_API_KEY, CLOUDINARY_API_SECRET:** Your credentials from your Cloudinary account.

## Usage

To run the application in development mode:

```bash
npm run dev
```

The API will be running on the port specified in your `.env` file (default: `8000`).

## API Endpoints

(You would typically list your main API endpoints here, e.g., `/api/v1/users/register`, `/api/v1/videos/upload`, etc., along with their methods and expected request/response formats. This section can be expanded once the API routes are fully defined and tested.)

## Contributing

Contributions are welcome! If you have any suggestions, bug reports, or want to contribute to the codebase, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the ISC License.
