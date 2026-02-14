<div align="center">

# 🚀 Day 2 – Backend, Database & GitHub

### Let’s turn our form into a real application

Today: Frontend → Server → Database 🌍

</div>

---

## 🎯 What We Will Achieve Today

By the end of this session you will:

✅ run a backend server
✅ connect MongoDB
✅ store form data permanently
✅ push updated code to GitHub

Massive upgrade from Day 1 🔥

---

# 🧩 Step 1 – Create `server.js`

Inside the `server` folder, create a file:

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

app.use(cors());
app.use(express.json());

// MongoDB Connection
mongoose
  .connect(process.env.MONGO_URI)
  .then(() => console.log("✅ Database connected"))
  .catch((err) => console.log("❌ DB Error:", err));

// Schema
const registrationSchema = new mongoose.Schema({
  name: String,
  email: String,
  phone: String,
});

// Model
const Registration = mongoose.model("Registration", registrationSchema);

// Route
app.post("/register", async (req, res) => {
  try {
    const { name, email, phone } = req.body;

    await Registration.create({ name, email, phone });

    res.json({ message: "Registration successful" });
  } catch (error) {
    res.status(500).json({ message: "Server error" });
  }
});

// Start Server
const PORT = process.env.PORT || 5000;

app.listen(PORT, () => {
  console.log(`🚀 Server running on port ${PORT}`);
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
  "description": "Backend for workshop",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "cors": "^2.8.5",
    "dotenv": "^16.4.5",
    "express": "^4.18.2",
    "mongoose": "^8.3.3"
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
MONGO_URI=PASTE_YOUR_MONGODB_URI_HERE
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
🚀 Server running on port 5000
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
