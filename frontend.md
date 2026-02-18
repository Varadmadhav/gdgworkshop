<div align="center">

# 🎉 Event Registration –  Workshop

Build your first working website in under 60 minutes 🚀  
No coding experience required.

[![Level](https://img.shields.io/badge/Level-Beginner-brightgreen)]()
[![Tech](https://img.shields.io/badge/Tech-HTML%20CSS%20JS-blue)]()
[![Workshop](https://img.shields.io/badge/Format-Hands--On-orange)]()

</div>

---



## 📂 Step 1 – Create Project Folder

Create a new folder on your computer:

```bash
event-registration

```

## 📄 Step 2 – Create `index.html`

```
index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Event Registration</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <div class="container">
    <h1>Register for the Event</h1>

    <form id="registrationForm">
      <input type="text" placeholder="Full Name" required />
      <input type="email" placeholder="Email Address" required />
      <input type="tel" placeholder="Phone Number" required />
      <button type="submit">Register</button>
    </form>

    <p id="message"></p>
  </div>

  <script src="script.js"></script>
</body>
</html>
```

 ---
## 🎨 Step 3 – Create `style.css`



```style.css


body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: linear-gradient(135deg, #667eea, #764ba2);
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  background: white;
  padding: 30px;
  border-radius: 10px;
  width: 320px;
  text-align: center;
}

h1 {
  margin-bottom: 20px;
}

input {
  width: 100%;
  padding: 10px;
  margin: 8px 0;
}

button {
  width: 100%;
  padding: 10px;
  background: #667eea;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background: #5a67d8;
}

#message {
  margin-top: 10px;
  color: green;
}
```

## ⚙️ Step 4 – Create `script.js`
```
const form = document.getElementById("registrationForm");
const message = document.getElementById("message");

form.addEventListener("submit", function (e) {
  e.preventDefault();

  message.textContent = "Registered successfully!";
  form.reset();
});

```

## 🚀 Step 5 – `Run the Project`
```
Right click index.html →
Open with Live Server

```



<div align="center">

# ☁️ Upload Your Project to GitHub

### End of Day 1 Submission Guide

Save your work online • Build your developer profile • Don’t lose progress 🚀

</div>

---

## 🎯 Goal

By the end of this section, your project should be visible in your GitHub repository.

---

## ✅ Step 1 – Create a New Repository

Go to GitHub and create a new repository.

Suggested name:

```bash
event-registration-frontend
```

Click **Create repository**.

---

## ✅ Step 2 – Open Terminal in VS Code

In VS Code:

**Terminal → New Terminal**

---

## ✅ Step 3 – Initialize Git

```bash
git init
```

---

## ✅ Step 4 – Add Your Files

```bash
git add .
```

---

## ✅ Step 5 – Commit Your Work

```bash
git commit -m "Day 1 frontend completed"
```

---

## ✅ Step 6 – Connect to GitHub

Copy your repository URL from GitHub and run:

```bash
git remote add origin YOUR_REPO_LINK
```

Example:

```bash
git remote add origin https://github.com/username/event-registration-frontend.git
```

---

## ✅ Step 7 – Push Code

```bash
git branch -M main
git push -u origin main
```

---

## 🎉 Verify Upload

Refresh your repository page on GitHub.

If you see:

✅ index.html
✅ style.css
✅ script.js

You did it 🔥

You are now using version control like real developers.

---

# ❓ Git Not Installed?

No problem 👍 You can still upload.

### Alternative Method:

1. Open your GitHub repository
2. Click **Add file → Upload files**
3. Drag and drop your project files
4. Click **Commit**

Done 🚀

---


<div align="center">

## 🚀 See you in Day 2 – Backend & Database

</div>

