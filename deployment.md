<div align="center">

# 🌍 Deployment Day – Go Live

### Backend + Frontend on the Internet 🚀

Laptop → Cloud → Public URL

</div>

---

## 🎯 Goal

By the end of this guide:

✅ backend will be live
✅ frontend will be live
✅ both will talk to each other
✅ you can open it from mobile 🌍

---

# 🧠 Architecture After Deployment

Frontend (public) → Backend API (public) → Database

---

# ☁️ Part 1 – Deploy Backend on Render

---

## ✅ Step 1 – Push Latest Code

Inside your project:

```bash
git add .
git commit -m "ready for deployment"
git push
```

---

## ✅ Step 2 – Open Render

👉 [https://render.com](https://render.com)
Login using GitHub.

---

## ✅ Step 3 – New Web Service

Click:

**New → Web Service**

Select your backend repository.

---

## ✅ Step 4 – Configuration

Fill values:

**Build Command**

```bash
npm install
```

**Start Command**

```bash
node server.js
```

---

## ✅ Step 5 – Environment Variables

Add:

```
Key: MONGO_URI
Value: your mongo string
```

```
Key: PORT
Value: 5000
```

---

## ✅ Step 6 – Deploy

Click **Create Web Service** and wait.

⏱ Takes around 2–5 minutes.

---

## 🎉 Step 7 – Copy Backend URL

You will get something like:

```
https://your-app.onrender.com
```

Your API endpoint becomes:

```
https://your-app.onrender.com/register
```

Save this link. We need it for frontend.

---

# 🔐 Update CORS in Backend (VERY IMPORTANT)

Open `server.js`.

Find:

```javascript
app.use(cors());
```

Replace with:

```javascript
app.use(cors({
  origin: "FRONTEND_URL_HERE"
}));
```

Example:

```javascript
app.use(cors({
  origin: "https://yourfrontend.vercel.app"
}));
```

Commit & push again:

```bash
git add .
git commit -m "cors updated"
git push
```

Render will auto redeploy.

---

# 🎨 Part 2 – Deploy Frontend

We will use Netlify.

---

## ✅ Step 1 – Update API URL in script.js

Replace localhost with your Render link.

```javascript
https://your-app.onrender.com/register
```

Save file.

---

## ✅ Step 2 – Push Changes

```bash
git add .
git commit -m "production api"
git push
```

---

## ✅ Step 3 – Open Netlify

👉 [https://netlify.com](https://netlify.com)
Login with GitHub.

---

## ✅ Step 4 – Deploy Using Drag & Drop (Fastest)

In Netlify dashboard, scroll to **Deploy manually**.

You will see a box that says **Drag and drop your site folder here**.

Open your project folder on your computer and drag the **frontend folder** (where `index.html` exists) into that box.

---

## ✅ Step 5 – Wait for Upload

Netlify will automatically upload and publish your site.

No build command needed for HTML/CSS/JS 🎉

---

## 🎉 Step 6 – Get Frontend URL

You will receive something like:

```
https://yourproject.netlify.app
```

Copy this link.

---

# 🔁 Final Step – Add This URL to Backend CORS

Go back to `server.js` and set:

```javascript
app.use(cors({
  origin: "https://yourproject.netlify.app"
}));
```

Push again:

```bash
git add .
git commit -m "final cors"
git push
```

Render will redeploy automatically.

---

# 🧪 Final Test

Open frontend URL → submit form.

If entry appears in MongoDB → LEGEND 🔥

---

# 🏆 What You Just Did

You built production architecture:

✅ UI
✅ API
✅ Database
✅ Cloud hosting

This is how startups ship products.

---

<div align="center">

## 📸 Take a screenshot & celebrate 🚀

</div>
