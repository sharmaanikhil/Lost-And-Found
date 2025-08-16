# Lost and Found - Full Stack MERN Application

[![Frontend](https://img.shields.io/badge/frontend-React-blue)](https://remarkable-donut-2e7e0e.netlify.app/)  
[![Backend](https://img.shields.io/badge/backend-Node.js-green)](https://c2911263-d706-4fcf-947d-769c4a5bdc56-00-rcs1k0rtl1n0.pike.replit.dev/)

---

## Project Overview
**Lost and Found** is a full-stack MERN (MongoDB, Express.js, React, Node.js) web application that enables users to report and track lost and found items in a particular area. The platform provides a centralized location for reporting lost and found items, making it easier for people to reunite lost belongings with their rightful owners. Users can create accounts, post reports, search for lost or found items, and leave comments to improve recovery chances.

---

## Live Demo
- **Frontend:** [https://remarkable-donut-2e7e0e.netlify.app/](https://remarkable-donut-2e7e0e.netlify.app/)  
- **Backend API:** [https://c2911263-d706-4fcf-947d-769c4a5bdc56-00-rcs1k0rtl1n0.pike.replit.dev/](https://c2911263-d706-4fcf-947d-769c4a5bdc56-00-rcs1k0rtl1n0.pike.replit.dev/)  

---

## Features

- User registration, login, and authentication
- Report lost items or found items with descriptions and images
- Search and filter reports based on location and category
- Comment on reports to provide additional information
- Image uploads handled with Firebase Storage integration
- Secure backend with JWT authentication and protected routes

---

## Tech Stack

| Layer          | Technology                                   |
| -------------- | --------------------------------------------|
| Frontend       | React.js, Axios                              |
| Backend        | Node.js, Express.js                          |
| Database       | MongoDB Atlas, Mongoose                      |
| Storage        | Firebase Storage                             |
| Authentication | JWT (JSON Web Tokens), bcrypt                |
| Hosting        | Netlify (Frontend), Replit (Backend)         |

---

## Architecture Overview
- React frontend communicates with a Node.js/Express backend via REST APIs.
- Backend handles user authentication, item reports, comments, and image uploads.
- MongoDB Atlas stores user data and reports securely.
- Firebase Storage is used to store images associated with items.
- CORS configured to allow secure communication between deployed frontend and backend.

---

## Installation & Local Setup

### Prerequisites
- Node.js (v14+)
- npm or yarn
- MongoDB Atlas account (for the database)
- Firebase account and project (for file storage)
- Git

### Steps

1. **Clone the repository**
git clone https://github.com/sharmaanikhil/Lost-And-Found.git
cd Lost-And-Found

2. **Backend Setup**
cd backend
npm install

- Create a `.env` file in the backend root directory with your environment variables:
PORT=4000
DB=your_mongodb_connection_string
SECRET_KEY=your_jwt_secret


- Start the backend server:
npm run start

3. **Frontend Setup**
cd ../client
npm install

- Update `firebase.js` with your Firebase project configuration.
- Update all backend URLs in frontend code to your backend server URL.
- Run frontend locally:
npm run dev

---

## Deployment

- The **frontend** is deployed on Netlify at:  
  [https://remarkable-donut-2e7e0e.netlify.app/](https://remarkable-donut-2e7e0e.netlify.app/)
- The **backend** is deployed on Replit at:  
  [https://c2911263-d706-4fcf-947d-769c4a5bdc56-00-rcs1k0rtl1n0.pike.replit.dev/](https://c2911263-d706-4fcf-947d-769c4a5bdc56-00-rcs1k0rtl1n0.pike.replit.dev/)

### Important Notes on Deployment

- CORS origin in the backend is configured to accept requests **only** from the Netlify frontend URL.
- When changing frontend URLs or deployment URLs in future, update the backend CORS allowed origins accordingly.
- Ensure MongoDB Atlas allows connections from your backend environment's IP.
- Firebase config must correspond to your Firebase project used for storage.

---

## Folder Structure
/backend
/controllers
/models
/routes
/middlewares
app.js
package.json
/frontend (or /client)
/src
/components
/pages
firebase.js
App.jsx
package.json

---

## Future Improvements

- Add multidimensional search (e.g., by date, location proximity).
- Implement push notifications or email alerts for matched found items.
- Enhance user profile with more customization and item tracking features.
- Integrate payments or premium features for priority listings.
- Add admin dashboard for moderation and site analytics.

---

## License

[MIT License](LICENSE)

---
