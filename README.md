<div align="center">

# 🎉 Event Registration – Frontend Workshop

Build your first working website in under 60 minutes 🚀  
No coding experience required.

[![Level](https://img.shields.io/badge/Level-Beginner-brightgreen)]()
[![Tech](https://img.shields.io/badge/Tech-HTML%20CSS%20JS-blue)]()
[![Workshop](https://img.shields.io/badge/Format-Hands--On-orange)]()

</div>

---

## 📌 What You Are Building

A clean and responsive event registration form that:

✅ collects user details  
✅ shows success message  
✅ prepares for backend connection  

---

## 🧠 What You Will Learn

- How project files are structured  
- How HTML, CSS & JS connect  
- How forms work  
- How real developers start from templates  

---

## 🧑‍💻 Prerequisites

Make sure you have:

- VS Code  
- Live Server extension  

---

## 📂 Step 1 – Create Project Folder

Create a new folder on your computer:

```bash
event-registration

```

📄 Step 2 – Create index.html

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

Step 3 – Create style.css

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

⚙️ Step 4 – Create script.js
```
const form = document.getElementById("registrationForm");
const message = document.getElementById("message");

form.addEventListener("submit", function (e) {
  e.preventDefault();

  message.textContent = "Registered successfully!";
  form.reset();
});

```

🚀 Step 5 – Run the Project
```
Right click index.html →
Open with Live Server

<div align="center">
⭐ If you enjoyed, don’t forget to star the repo!
</div>
```
