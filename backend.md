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

# 🧩 Step 1 – Get the Backend Template

Create a new folder inside your project:

```bash
server
```

Your mentor will provide the backend files.

Add these inside the `server` folder:

```bash
server.js
package.json
.env.example
```

---

# 📦 Step 2 – Install Dependencies

Open terminal inside the **server** folder and run:

```bash
npm install
```

This downloads everything the server needs.

---

# 🔐 Step 3 – Setup Environment Variables

We never store secrets directly in code.

Create a new file:

```bash
.env
```

Copy content from `.env.example` and paste your MongoDB connection string.

Example:

```bash
MONGO_URI=your_link_here
PORT=5000
```

Save the file ✅

---

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

If you see this → YOU ARE A BACKEND DEVELOPER TODAY 😎

---

# 🔄 Step 5 – Connect Frontend to Backend

Now the form will send data to:

```bash
http://localhost:5000/register
```

When you submit the form → data goes to database 🔥

Ask mentor to show live entries.

---

# ☁️ Step 6 – Push Backend to GitHub

Let’s save today’s progress online.

---

## Initialize Git (if needed)

```bash
git init
```

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

---

## Connect Repository

```bash
git remote add origin YOUR_REPO_LINK
```

(If already connected, skip this step.)

---

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

## 💥 Tomorrow / Next: Deployment & Going Live

</div>
