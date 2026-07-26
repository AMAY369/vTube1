# vTube — Video Streaming Platform

A full-stack video streaming application: users can sign up, upload and watch videos, subscribe to channels, and comment — with JWT authentication over an Express/MongoDB REST API.

<!-- The old Vercel deployment (v-tube-clone.vercel.app) is returning 404 — redeploy it,
     then restore this line. A working demo is the single strongest thing on this page.
**Live demo:** https://v-tube-clone.vercel.app
-->

<!-- Add a screenshot or short GIF here — it is the single biggest improvement you can make to this README.
     Put the file in docs/ and reference it:
![vTube home page](docs/screenshot-home.png)
-->

## Features

- **Authentication** — signup and login with bcrypt-hashed passwords, JWT tokens issued and carried in HTTP-only cookies
- **Video** — upload, stream, and play back videos
- **Engagement** — like, comment, and subscribe to channels
- **Search** — search and filter the video catalog
- **Profiles** — user profile and channel management

## Tech Stack

| Layer | Technologies |
| --- | --- |
| Frontend | React, React Router, Material UI, styled-components, Axios, React Toastify |
| Backend | Node.js, Express, Mongoose |
| Database | MongoDB |
| Auth | JSON Web Tokens (JWT), bcrypt, cookie-parser |
| Deployment | Vercel |

## Project Structure

```
vTube1/
├── client/          # React front end (Vite)
│   └── src/
└── server/          # Express REST API
    ├── controllers/
    ├── models/      # user, video, comment
    ├── routes/      # user, video, comment, search
    ├── middlewares/
    └── db/
```

## API Overview

| Resource | Routes |
| --- | --- |
| `user` | registration, login, profile, subscribe |
| `video` | create, fetch, stream, like |
| `comment` | add and list comments on a video |
| `search` | query and filter videos |

## Getting Started

**Prerequisites:** Node.js 18+ and a MongoDB database (local or MongoDB Atlas).

```bash
git clone https://github.com/AMAY369/vTube1
cd vTube1
```

**1. Backend**

```bash
cd server
npm install
cp .env.example .env      # then fill in your own values
npm start
```

**2. Frontend**

```bash
cd client
npm install
npm run dev
```

### Environment Variables

Create `server/.env` from `server/.env.example`:

| Variable | Description |
| --- | --- |
| `PORT` | Port the API listens on (e.g. `8000`) |
| `MONGODB_URI` | MongoDB connection string |
| `JWT_SECRET_KEY` | Secret used to sign JWT auth tokens |

Generate a strong JWT secret:

```bash
node -e "console.log(require('crypto').randomBytes(48).toString('hex'))"
```

> `.env` is git-ignored. Never commit real credentials.

## Author

**Abhay Gupta** — [GitHub](https://github.com/AMAY369) · [LinkedIn](https://linkedin.com/in/abhayg369)
