# Video Streaming Platform API 🎥

[![Node.js](https://img.shields.io/badge/Node.js-18%2B-green)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-blue)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6%2B-brightgreen)](https://www.mongodb.com/)

A robust backend API for a YouTube-like video streaming platform with complete user authentication, video management, and social engagement features.

## ✨ Features

### 🔐 Authentication

- JWT-based user registration/login
- Password encryption
- Refresh token rotation
- Protected routes middleware

### 🎬 Video Management

- Video upload with thumbnails (Cloudinary storage)
- CRUD operations for videos
- Views tracking system
- Published/unpublished status toggle

### 💬 Engagement Features

- Comment system with replies
- Like/dislike functionality for videos, comments, and tweets
- Playlist creation and management
- Channel subscription system
- Tweet functionality

### 📊 Analytics

- Channel dashboard
- User watch history
- Liked videos
- Subscriber

## 🛠 Technologies Used

| Category       | Technologies                |
| -------------- | --------------------------- |
| Backend        | Node.js, Express.js         |
| Database       | MongoDB (with Mongoose ODM) |
| Authentication | JWT, Bcrypt                 |
| File Storage   | Cloudinary                  |
| Middleware     | Multer                      |
| Utilities      | Nodemon, Dotenv             |

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (v6 or higher)
- Cloudinary account

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/video-streaming-api.git
cd video-streaming-api
```

2. Install dependencies:

```bash
# Installation
npm install

# Set up environment
cp .env.example .env
# Edit the .env file with your credentials

# Start development server
npm run dev

# Production start
npm start
```

# Environment Variables

# Server Configuration

PORT=8000
NODE_ENV=development

# Database

MONGODB_URI=mongodb://localhost:27017/videostream

# Cloudinary

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# JWT

ACCESS_TOKEN_SECRET=your_random_access_token_secret
REFRESH_TOKEN_SECRET=your_random_refresh_token_secret
ACCESS_TOKEN_EXPIRY=15m
REFRESH_TOKEN_EXPIRY=7d

# API Endpoints

## Authentication

| Endpoint             | Method | Description          | Request Body                                  |
| -------------------- | ------ | -------------------- | --------------------------------------------- |
| /users/register      | POST   | Register new user    | {username, email, fullName, password, avatar} |
| /users/login         | POST   | User login           | {email/username, password}                    |
| /users/logout        | POST   | User logout          | Requires valid refresh token                  |
| /users/refresh-token | POST   | Refresh access token | {refreshToken}                                |
| /users/profile       | GET    | Get user profile     | Requires valid access token                   |
| /users/profile       | PUT    | Update user profile  | {fullName, email, password}                   |

# Videos

| Endpoint                        | Method | Description                |
| ------------------------------- | ------ | -------------------------- |
| /videos                         | GET    | Get all videos (paginated) |
| /videos                         | POST   | Upload new video           |
| /videos/:videoId                | GET    | Get video details          |
| /videos/:videoId                | PATCH  | Update video metadata      |
| /videos/:videoId                | DELETE | Delete video               |
| /videos/toggle/publish/:videoId | PATCH  | Toggle publish status      |

# Comments

| Endpoint               | Method | Description        |
| ---------------------- | ------ | ------------------ |
| /comments/:videoId     | GET    | Get video comments |
| /comments/:videoId     | POST   | Add new comment    |
| /comments/c/:commentId | PATCH  | Update comment     |
| /comments/c/:commentId | DELETE | Delete comment     |

# Project Structure

```bash
video-streaming-api/
├── src/ # Source files
│   ├── db/ # Database configuration files
│   ├── controllers/ # Route controllers
│   ├── models/ # MongoDB models
│   ├── routes/ # API routes
│   ├── utils/ # Utility functions
│   ├── middlewares/ # Custom middlewares
│   ├── utils/ # Utility functions
│   ├── .env.example # Environment variables template
│   ├── app.js # Express application
│   └── constants.js # Constants
│   └── index.js # Server entry point
```
