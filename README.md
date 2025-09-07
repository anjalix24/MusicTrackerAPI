## 🎵Music Tracker API

A local RESTful API which is made by using Node.js, Express.js and SQLite3 that allows users to manage a list of songs and playlists. We can perform tasks like creating,viewing and playing a song, as well as creating, viewing and running a playlist. Optionally includes a basic frontend to interact with the API.

## 📁 Project Structure

📁 MusicTrackerAPI  
├── _tests/  
│   ├── api/  
│   ├── integration/  
│   └── unit/                    
├── controllers/  
│   └── songController.js       
├── routes/  
│   └── songRoutes.js          
├── music.db                   
├── db.js                      
├── server.js                  
├── MusicAPI.html              
├── package.json                
├── coverage/                   
├── .github/workflows/          
├── appss.png  
├── appss2.png       
└── README.md  
              
## 📌 Features

✅ Create, view and play songs and playlists using API  <br>
✅ Local database using SQLite3  <br>
✅ Integrated with DB Browser for SQLite3  <br>
✅ HTML frontend (optional)  <br>
✅ Backend using Node.js and Express.js  <br>
✅ Fully local setup — no external APIs used  <br>

## 🚀 How to Run This Project

1. 📥 Clone the Repository
   `git clone https://github.com/your-username/music-tracker-api.git` <br>
   `cd music-tracker-api`

2. 📦 Install Dependencies
   Node.js (v14 or above)  <br>
→ Required to run the backend server.  <br>
  npm (Node Package Manager)  <br>
  `npm install`  <br>
→ Comes with Node.js. Used to install project dependencies.  <br>

3. ✅ Start the Server  <br>
  Run this command :  <br>
   `node server.js`  <br>
   The server will start at: <br>
   http://localhost:5000  <br>

## 🧠 API Endpoints

GET /api/songs  <br>
Returns all songs in the database.  <br>
Response:  
```json

  {
    "id": 1,
    "title": "Test Song",
    "artist": "Tester",
    "genre": "Rock"
  }
```

POST /api/songs  <br>
Adds a new song to the database.  <br>
Request Body:  
```json
{
  "title": "Shape of You",
  "artist": "Ed Sheeran",
  "genre": "Pop"
}
```

Response:
```json
{
  "id": 2,
  "title": "Shape of You",
  "artist": "Ed Sheeran",
  "genre": "Pop"
}
```

## 🗃️ Database Used

📌 SQLite Database File: music.db  <br>
🎛️ Managed Using: DB Browser for SQLite  <br>
🛠️ Tables are auto-created on server start (via db.js)  <br>

## 🎼 Table Schema:

```sql
CREATE TABLE IF NOT EXISTS songs (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT,
  artist TEXT,
  genre TEXT
);
```

## 🌐 Frontend

You can easily run the frontend by opening the MusicAPI.html file in your browser. <br>
🔧 Features: <br>
🎵 Add a song using a simple form <br>
📋 View all added songs in a list <br>

## 🚀 How to Use:

Make sure your server is running (node server.js) <br>
Double-click on MusicAPI.html to open it in your browser <br>
Fill out the form and hit “Add Song” to submit 🎶 <br>

## Sample curl Requests
* 🎵 Add a New Song
```bash
Copy
Edit
curl -X POST http://localhost:5000/api/songs \
  -H "Content-Type: application/json" \
  -d '{
    "title": "Test Song",
    "artist": "Tester",
    "genre": "Rock"
  }'
```
* Get All Songs:  
```bash
curl http://localhost:5000/api/songs
```
## 🛠️ Built With  <br>

- 🟩 **Node.js** – For backend JavaScript runtime  <br>
- 🚂 **Express.js** – Web framework to handle routes and APIs  <br>
- 🗃 **SQLite3** – Lightweight database for storage  <br>
- 🌐 **HTML/CSS/JavaScript** – To power the frontend UI  <br>

## ⚙️ Prerequisites

Before you begin, make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or above)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- A code editor like [VS Code](https://code.visualstudio.com/)
- [DB Browser for SQLite](https://sqlitebrowser.org/) (optional, for exploring `music.db`)

---

## 🔄 Resetting the Database

- The database is stored in the file **`music.db`**.
- To reset your data, simply delete the `music.db` file and restart the server:
  ```bash
  rm music.db
  node server.js



Contribute by:

1.Fork this repository.

2.Create a new branch (git checkout -b my-feature).

3.Make your changes and commit (git commit -m "Added new feature").

4.Push to your branch (git push origin my-feature).

5.Open a Pull Request


## 📄 License  <br>

This project is **open-source** and free to use!  <br>
Feel free to **fork it**, **play around**, or even use it to build something cooler.  <br>
Just don’t forget to give credit if you’re vibing with it 💫  
