<div align="center">

# 🎉 Event Registration –  Workshop

Build your first working website 🚀  
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
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>Full Stack Workshop Registration</title>

<link rel="stylesheet" href="style.css">

<!-- MODERN FONT -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

</head>
<body>

<div class="container">

<h1>🚀 Event Registration Form</h1>
<p>Register now to secure your spot!</p>

<form id="registrationForm">

<div class="form-group">
<label>Full Name</label>
<input type="text" id="name" placeholder="Enter your full name" required>
</div>

<div class="form-group">
<label>Email Address</label>
<input type="email" id="email" placeholder="Enter your email" required>
</div>

<div class="form-group">
<label>Phone Number</label>
<input type="tel" id="phone" placeholder="Enter phone number" required>
</div>

<div class="form-group">
<label>College Name</label>
<input type="text" id="college" placeholder="Enter your college name" required>
</div>

<div class="form-group">
<label>Select Year</label>
<select id="year" required>
<option value="">-- Select Year --</option>
<option>1st Year</option>
<option>2nd Year</option>
<option>3rd Year</option>
<option>4th Year</option>
</select>
</div>

<div class="form-group">
<label>Branch</label>
<input type="text" id="branch" placeholder="Enter your branch" required>
</div>

<div class="form-group">
<label>Select Event Type</label>
<select id="event" required>
<option value="">-- Select --</option>
<option value="Workshop">Workshop</option>
<option value="Seminar">Seminar</option>
<option value="Hackathon">Hackathon</option>
</select>
</div>

<button type="submit">Register</button>
<button type="reset" class="reset">Clear</button>

</form>

<div id="successMessage" class="success"></div>

</div>

<script src="script.js"></script>
</body>
</html>
```

 ---
## 🎨 Step 3 – Create `style.css`



```
* {
margin: 0;
padding: 0;
box-sizing: border-box;
font-family: 'Poppins', sans-serif;
}

body {
background: linear-gradient(135deg, #667eea, #764ba2);
min-height: 100vh;
display: flex;
align-items: center;
justify-content: center;
}

.container {
background: rgba(255,255,255,0.9);
padding: 35px;
width: 450px;
border-radius: 15px;
box-shadow: 0 20px 50px rgba(0,0,0,0.3);
backdrop-filter: blur(10px);
animation: fadeIn 0.8s ease-in-out;
}

.container h1 {
text-align: center;
margin-bottom: 10px;
}

.container p {
text-align: center;
margin-bottom: 20px;
color: #555;
}

.form-group {
margin-bottom: 15px;
}

label {
font-weight: 600;
display: block;
margin-bottom: 5px;
}

input, select {
width: 100%;
padding: 12px;
border-radius: 8px;
border: 1px solid #ccc;
transition: 0.3s;
}

input:focus, select:focus {
border: 1px solid #667eea;
box-shadow: 0 0 8px #667eea;
outline: none;
}

button {
width: 100%;
padding: 12px;
background: linear-gradient(135deg,#667eea,#764ba2);
border: none;
color: white;
font-size: 16px;
border-radius: 8px;
cursor: pointer;
margin-top: 10px;
transition: 0.3s;
}

button:hover {
transform: scale(1.05);
box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

.reset {
background: #999;
}

.reset:hover {
background: #777;
}

.success {
margin-top: 15px;
text-align: center;
font-weight: bold;
}

@keyframes fadeIn {
from {opacity:0; transform:translateY(30px);}
to {opacity:1; transform:translateY(0);}
}



```

## ⚙️ Step 4 – Create `script.js`
```
const form = document.getElementById("registrationForm");
const successMessage = document.getElementById("successMessage");

form.addEventListener("submit", async function (e) {
e.preventDefault();

const data = {
name: document.getElementById("name").value,
email: document.getElementById("email").value,
phone: document.getElementById("phone").value,
college: document.getElementById("college").value,
year: document.getElementById("year").value,
branch: document.getElementById("branch").value,
event: document.getElementById("event").value
};

try {

const res = await fetch("http://localhost:5000/register", {
method: "POST",
headers: { "Content-Type": "application/json" },
body: JSON.stringify(data)
});

const result = await res.json();

successMessage.innerText = result.message;
form.reset();

} catch (error) {

successMessage.innerText = "❌ Server Error!";

}

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

