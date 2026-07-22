# airbnb-clone
This clone of airbnb using MERN stack
# 🏠 Airbnb Clone — MERN Stack

A full-stack Airbnb clone built with **MongoDB, Express, React, and Node.js**. Users can browse listings, register/login, list their own places, upload photos, and book stays with check-in/check-out dates.

## ✨ Features

- User authentication (register/login/logout) with JWT stored in cookies and bcrypt-hashed passwords
- Create, edit, and browse place listings (title, description, address, price, perks, check-in/out times, max guests)
- Photo uploads — either from a device or by pasting an image link — stored via Cloudinary
- Book a place with check-in/check-out dates, guest count, and contact info
- View your own listings and your booking history
- Responsive UI styled with TailwindCSS

## 🛠️ Tech Stack

**Client:** React 18, React Router, Vite, TailwindCSS, Axios, date-fns

**Server:** Node.js, Express, MongoDB (Mongoose), JWT, bcrypt, Multer, Cloudinary

## 📁 Project Structure

```
├── client/          # React frontend (Vite)
│   └── src/
│       ├── components/   # Pages & UI components (Home, Login, Register, PlacesForm, Bookings, etc.)
│       ├── App.jsx
│       ├── Layout.jsx
│       └── userContext.jsx
├── api/              # Express backend
│   ├── models/        # Mongoose schemas: User, Place, Booking
│   └── index.js        # API routes & server entry point
└── vercel.json
```

## 🚀 Run Locally

Clone the project:

```bash
git clone https://github.com/Mehulparekh144/Airbnb-Clone-using-MERNStack.git
cd Airbnb-Clone-using-MERNStack
```

Install and run the backend:

```bash
cd api
npm install
nodemon index.js
```

Install and run the frontend (in a separate terminal):

```bash
cd client
npm install
npm run dev
```

The frontend runs on `http://127.0.0.1:5173` and the API on `http://localhost:4000`.

## 🔑 Environment Variables

Create a `.env` file inside the `api` folder with:

```
MONGO_URL=your_mongodb_atlas_connection_string
SECRET_KEY=any_random_secret_string
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

- `MONGO_URL` — get this from [MongoDB Atlas](https://www.mongodb.com/atlas)
- `SECRET_KEY` — any random string used to sign JWTs
- Cloudinary keys — get these from your [Cloudinary dashboard](https://cloudinary.com/) (used for photo uploads)

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/register` | Create a new user account |
| POST | `/api/login` | Log in and receive a JWT cookie |
| POST | `/api/logout` | Clear the auth cookie |
| GET | `/api/profile` | Get the logged-in user's profile |
| POST | `/api/upload-by-link` | Upload a photo via image URL (Cloudinary) |
| POST | `/api/upload` | Upload photos from device (Cloudinary) |
| POST | `/api/places` | Create a new place listing |
| GET | `/api/user-places` | Get listings owned by the logged-in user |
| GET | `/api/places/:id` | Get a single place by ID |
| PUT | `/api/places` | Update a place listing |
| GET | `/api/places` | Get all place listings |
| POST | `/api/bookings` | Create a booking |
| GET | `/api/bookings` | Get bookings for the logged-in user |

## 👤 Author

-(https://www.github.com/Nandeesh650)

## 💬 Feedback

If you have any feedback, reach out at sbnandeesh03@gmail.com
