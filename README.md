# vTube

A video streaming platform built with the MERN stack. Users can sign up, upload and watch videos, and interact through likes, comments and subscriptions.

## Features

- User authentication with signup and login
- Video upload, streaming and playback
- Like, comment and subscribe
- Search and filter videos
- User profile management

## Tech Stack

**Frontend:** React, CSS
**Backend:** Node.js, Express
**Database:** MongoDB with Mongoose

## Getting Started

### Prerequisites

- Node.js 18 or later
- A MongoDB connection string

### Backend

```sh
cd server
npm install
```

Create a `.env` file in `server/`:

```
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

Then start it:

```sh
npm start
```

### Frontend

```sh
cd client
npm install
npm start
```

The app runs at `http://localhost:3000` and talks to the API on `http://localhost:5000`.

## Project Structure

```
client/   React frontend
server/   Express API, models and routes
```

## License

MIT
