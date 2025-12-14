# 📧 Web Mail Application

A **Node.js + Express web mail application** that allows users to send emails **with file attachments** using **Gmail OAuth2 authentication**.
The frontend is a simple HTML/CSS form, and the backend uses **Nodemailer, Multer, and Google APIs**.

---

## ✨ Features

* 📩 Send emails from a web form
* 📎 **File attachment upload (required)**
* 🔐 Gmail **OAuth2 authentication** (no plain passwords)
* 📨 Email sending via **Nodemailer**
* 📁 File handling using **Multer**
* 🌐 Express.js backend server
* 🎨 Clean HTML + CSS frontend
* 📄 Success confirmation page after email is sent
* 🔒 Environment variables using **dotenv**

---

## 📂 Project Structure

```
web-mail/
│
├── index.js
├── package.json
├── package-lock.json
├── attachments/
│
└── public/
    ├── index.html
    ├── index.css
    ├── success.html
    └── success.css
```

---

## 📄 File-by-File Explanation

### `index.js`

* Main server file
* Creates Express app
* Uses `multer` to handle file uploads
* Uses Gmail OAuth2 via `googleapis`
* Sends email with attachment using `nodemailer`
* Loads environment variables using `dotenv`
* Runs server on **port 3000**

---

### `package.json`

* Project metadata
* Dependencies used:

  * `express` – backend server
  * `nodemailer` – email sending
  * `multer` – attachment upload
  * `googleapis` – Gmail OAuth2
  * `dotenv` – environment variables
* Uses **nodemon** for development

---

### `attachments/`

* Stores uploaded attachment files
* Used by Multer before sending email

---

### `public/index.html`

* Email form UI
* Fields include:

  * Receiver email
  * Subject
  * Message body
  * **Attachment (required)**
* Submits form data to backend

---

### `public/index.css`

* Styling for email form
* Layout, buttons, spacing, fonts

---

### `public/success.html`

* Displayed after successful email delivery

---

### `public/success.css`

* Styling for success confirmation page

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
OAUTH_CLIENT_ID=your_google_client_id
OAUTH_CLIENT_SECRET=your_google_client_secret
OAUTH_REFRESH_TOKEN=your_refresh_token
SENDER_EMAIL=your_gmail_address
```

---

### 📌 Important Notes for OAuth2

* Gmail OAuth2 is required
* Client ID & Secret come from **Google Cloud Console**
* Refresh token is generated via OAuth consent
* Regular Gmail passwords will **not work**

---

## 🚀 How to Run the Project

### 1️⃣ Install Dependencies

```bash
npm install
```

---

### 2️⃣ Start the Server

```bash
npm start
```

(Server runs on **[http://localhost:3000](http://localhost:3000)**)

---

### 3️⃣ Open in Browser

```
http://localhost:3000
```

---

## 🛠 Technologies Used

* Node.js
* Express.js
* Nodemailer
* Multer
* Google APIs (Gmail OAuth2)
* dotenv
* HTML5
* CSS3

---

## 📜 License

MIT License
Free to use for learning and personal projects.

---
