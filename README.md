Here is a full `README.md` file for your **Story Comments App** using **React + Firebase Authentication + Express + MongoDB**:

---

````markdown
# 📝 Story Comments App

This project allows authenticated users to post and view comments on stories. It uses:
- **React** for frontend
- **Firebase Authentication** for user login (Google Sign-In)
- **Express** for backend API
- **MongoDB** for comment storage

---

## 🚀 Features

- 🔐 Google Sign-In using Firebase
- 💬 Post comments under stories
- 👤 Comment info includes user name, email, and profile image
- 📥 Comments are stored in MongoDB
- 🔄 Comments are fetched and displayed per story
- ⚡ Real-time update in UI after submitting comment

---

## 🛠 Tech Stack

- **Frontend**: React, Firebase Auth, Axios
- **Backend**: Node.js, Express.js, MongoDB, Mongoose
- **Authentication**: Firebase (Google Sign-In)
- **Database**: MongoDB

---

## 🔧 Installation and Setup

### 📁 1. Clone the Repo

```bash
git clone https://github.com/yourusername/story-comments-app.git
cd story-comments-app
````

---

### 🖥️ 2. Backend Setup

```bash
cd backend
npm install
```

#### Create a `.env` file:

```
PORT=5000
MONGO_URI=mongodb://localhost:27017/commentsdb
```

#### Start the backend server:

```bash
node server.js
```

✅ Should display:

```
MongoDB Connected
Server running on port 5000
```

---

### 🌐 3. Frontend Setup

```bash
cd ../story-comments
npm install
```

#### Configure Firebase:

Edit `src/firebase.js`:

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  appId: "YOUR_APP_ID"
};
```

Get this config from your [Firebase Console](https://console.firebase.google.com/).

---

### ▶️ 4. Run the React App

```bash
npm start
```

Visit: [http://localhost:3000](http://localhost:3000)

---

## 📦 Folder Structure

```
story-comments-app/
│
├── backend/
│   ├── models/Comment.js
│   ├── routes/comments.js
│   ├── server.js
│   └── .env
│
└── story-comments/
    ├── src/
    │   ├── components/Auth.js
    │   ├── components/CommentBox.js
    │   └── firebase.js
    ├── App.js
    └── package.json
```

---

## 📄 API Endpoints (Backend)

* `GET /api/comments/:storyId` – fetch all comments for a story
* `POST /api/comments` – submit a new comment

---

## 📌 Example Comment Schema

```json
{
  "storyId": "story-123",
  "userName": "Yasaswini",
  "userEmail": "yasaswini@example.com",
  "userImage": "https://example.com/photo.jpg",
  "commentText": "Great article!",
  "createdAt": "2025-06-30T18:00:00Z"
}
```

