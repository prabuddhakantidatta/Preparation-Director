# 🚀 How to Deploy Your WBCS 2026 Tracker to Firebase Hosting

Deploying your Single Page Application (index.html) to Firebase Hosting is easy and completely free!

## Prerequisites
- Make sure you have **Node.js** installed on your computer.
- Ensure you have signed up at [console.firebase.google.com](https://console.firebase.google.com).

---

## Step 1: Install Firebase CLI
Open your terminal (Mac/Linux) or Command Prompt/Git Bash (Windows) and install the Firebase CLI globally:

```bash
npm install -g firebase-tools
```

---

## Step 2: Login to Firebase
Authenticate the CLI with your Google Account:

```bash
firebase login
```
This will open a browser window for you to select your Google Account.

---

## Step 3: Initialize Firebase in Your Folder
Navigate to the directory where your `index.html` file is stored, and run:

```bash
firebase init hosting
```

During initialization, answer the prompts as follows:
1. **Project Setup**: Select `Use an existing project` and select `wbcs-progress-tracker-30fa6` (from your Firebase config).
2. **Public Directory**: Type `.` (just a period, which means the current folder where `index.html` is).
3. **Configure as a single-page app**: Type `y` (Yes).
4. **Set up automatic builds and deploys with GitHub?**: Type `n` (No, unless you want to).
5. **Overwrite index.html?**: Type `n` (No - very important! Do not overwrite your file).

---

## Step 4: Deploy Your App!
Once initialization is complete, you can deploy your site to the web with a single command:

```bash
firebase deploy
```

🎉 **Congratulations!** Firebase will give you a live URL like:
`https://wbcs-progress-tracker-30fa6.web.app` or `https://wbcs-progress-tracker-30fa6.firebaseapp.com`

---

## 🛠 Troubleshooting: Fixing "Server connection failed..."
Since you are using **Firebase Realtime Database and Auth instead of local node APIs**, you may have some hardcoded references to `localhost:5000`. 
The modern tracking system uses Firebase directly without relying on a localhost express server, so the app bypasses this error by talking to Firebase APIs directly!
