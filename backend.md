<div align="center">

# 🚀 Day 2 – Backend, Database & GitHub

### Let’s turn our form into a real application

Today: Frontend → Server → Database 🌍

</div>



# 🧩 Step 1 – Create `server.js`

Inside the `backend` folder, create a file:

```bash
server.js
```

### ✨ Paste this code:

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");
require("dotenv").config();

const app = express();

// Middleware
app.use(cors({
  origin: "http://127.0.0.1:5500",
  methods: ["GET", "POST"],
  allowedHeaders: ["Content-Type"],
}));
app.use(express.json());

// MongoDB Connection
mongoose.connect(process.env.MONGO_URI)
.then(() => console.log("✅ MongoDB Connected"))
.catch(err => console.log("❌ DB Error:", err));

// Schema
const registrationSchema = new mongoose.Schema({
  name: { type: String, required: true },
  email: { type: String, required: true },
  phone: { type: String, required: true },
  college: { type: String, required: true },
  year: { type: String, required: true },
  branch: { type: String, required: true },
  event: { type: String, required: true }
});

// Model
const Registration = mongoose.model("Registration", registrationSchema);

// API Route
app.post("/register", async (req, res) => {
  try {

    const newUser = new Registration(req.body);
    await newUser.save();

    res.json({
      message: "🎉 Registration Successful!"
    });

  } catch (err) {

    res.status(500).json({
      message: "❌ Error Saving Data"
    });

  }
});

// Server Start
app.listen(process.env.PORT, () => {
  console.log(`🚀 Server running on http://localhost:${process.env.PORT}`);
});
```

---

# 🧩 Step 2 – Create `package.json`

Create a new file:

```bash
package.json
```

### ✨ Paste this code:

```json
{
  "name": "event-registration-backend",
  "version": "1.0.0",
  "description": "Full Stack Workshop Backend",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "cors": "^2.8.5",
    "dotenv": "^16.4.5",
    "express": "^4.18.2",
    "mongoose": "^8.0.0"
  }
}
```

---

# 🧩 Step 3 – Create `.env`

Create a file:

```bash
.env
```

### ✨ Paste:

```
MONGO_URI= 
PORT=5000
```
Save the file ✅
---


# 📦 Step 4 – Install Dependencies

Open terminal inside the **server** folder and run:

```bash
npm install
```

This downloads everything the server needs.



# ▶️ Step 4 – Start the Server

```bash
node server.js
```

---

## 🎉 Success Output

If everything is correct, you should see:

```
✅ Database connected
🚀 Server running on http://localhost:5000
```

---

# 🔄 Step 5 – Connect Frontend to Backend

Now the form will send data to:

```bash
http://localhost:5000/register
```





---

# ☁️ Step 6 – Push Backend to GitHub

Let’s save today’s progress online.

---

## Add Files

```bash
git add .
```

---

## Commit

```bash
git commit -m "Day 2 backend connected"
```

## Push

```bash
git branch -M main
git push -u origin main
```

---

## 🎉 Verify

Refresh GitHub.

You should now see your backend folder uploaded 🚀

---

# ❓ Git Not Working?

Use manual upload:

1. Open repository on GitHub
2. Click **Add file → Upload files**
3. Drag the server folder
4. Commit

Continue learning 👍

---

# 🧠 What You Learned Today

You experienced real system design:

Frontend → API → Database → Internet

This is how actual products work.

---

<div align="center">

## 💥 Next: Deployment & Going Live

</div>
