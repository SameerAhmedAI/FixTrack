<div align="center">

  <img src="https://github.com/Muhammad-Ahmed-Rayyan/FixTrack/blob/main/Fixtrack.png" width="500">
  
  #
  
  <p><b>Real-Time Issue Reporting and Tracking System</b></p>

![Last Commit](https://img.shields.io/github/last-commit/Muhammad-Ahmed-Rayyan/FixTrack)
![TypeScript](https://img.shields.io/badge/TypeScript-61.9%25-blue?logo=typescript)
![CSS](https://img.shields.io/badge/CSS-37.2%25-orange?logo=css3)
![languages](https://img.shields.io/github/languages/count/Muhammad-Ahmed-Rayyan/FixTrack)

<br>

Built with the tools and technologies: 

![React](https://img.shields.io/badge/React-%2361DAFB.svg?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-%23FFCA28.svg?style=for-the-badge&logo=firebase&logoColor=c1121f)
![TypeScript](https://img.shields.io/badge/TypeScript-%233178C6.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Leaflet](https://img.shields.io/badge/Leaflet-%23199900.svg?style=for-the-badge&logo=leaflet&logoColor=white)
![Cloudinary](https://img.shields.io/badge/Cloudinary-%233498DB.svg?style=for-the-badge&logo=cloudinary&logoColor=white)

</div>

---

## 🧠 Project Summary

**FixTrack** is a web-based application designed for real-time reporting, tracking, and resolution of issues. It provides a platform for users to submit issues with location data, and for administrators to manage and monitor the status of these issues. The interactive map interface allows for easy visualization of issue locations and supports department-based management for better organization.

🔗 Check it out: [FixTrack](https://fixtrack-app.firebaseapp.com/)

---

## 🚀 Features

- 🔐 **User Authentication:** Secure user registration and login functionality.
- 🗺️ **Interactive Map:** Users can report issues by selecting a location on an interactive map powered by **Leaflet**.
- 📝 **Issue Reporting:** Submit detailed reports including title, description, image (via **Cloudinary**), and location.
- 📊 **Dashboard:** View, filter, and manage all reported issues in one place.
- 🔔 **Real-Time Updates:** Issue data and statuses update in real-time through **Firebase**.
- 🤖 **Chatbot Integration:** An intelligent chatbot assists users with reporting or tracking issues.
- 👥 **Role-Based Access:**
  - **Department Admins** can view and manage reports related only to their respective departments (e.g., road, sanitation, etc.).
  - **Super Admins** have full access — they can view/manage all reports and handle user management.
- 🧭 **Location-Based Reporting:** Each issue is tagged with its geographic coordinates for accurate placement on the map.
- 🎨 **Responsive Design:** Fully responsive and mobile-friendly UI built with **React** and custom **CSS**.

---

## 🔧 Setup & Installation

> Make sure **Node.js** and **npm** are installed on your system.

```bash
# Clone the repo
git clone https://github.com/Muhammad-Ahmed-Rayyan/FixTrack.git
cd FixTrack

# Install required libraries
npm install

# Run the development server
npm run dev
```

---

## 🔑 API Configuration

To ensure FixTrack runs properly with all connected services (Firebase, Gemini, and Cloudinary), you need to replace configuration values inside the existing project files.

### ⚙️ 1. Environment Variables — FixTrack/.env

Replace the existing values in your .env file with the following environment variables:
```.env
VITE_API_KEY="YOUR-FIREBASE-CONSOLE-APP-API-KEY"
VITE_AUTH_DOMAIN="YOUR-FIREBASE-CONSOLE-APP-AUTH-DOMAIN"
VITE_PROJECT_ID="YOUR-FIREBASE-CONSOLE-APP-PROJECT-ID"
VITE_STORAGE_BUCKET="YOUR-FIREBASE-CONSOLE-APP-STORAGE-BUCKET"
VITE_MESSAGING_SENDER_ID="YOUR-FIREBASE-CONSOLE-APP-MESSAGING-SENDER-ID"
VITE_APP_ID="YOUR-FIREBASE-CONSOLE-APP-ID"
VITE_GEMINI_API_KEY="YOUR-GEMINI-API-KEY"
```
You can obtain these values from:

- Firebase Console:
  - Go to your Firebase project → Project Settings → General.
  - Under Your Apps, select your web app to view the configuration keys.

- Gemini API (for AI Integration):
  - Visit [Google AI Studio](https://makersuite.google.com/app/apikey) to generate your Gemini API Key.
  -Replace "YOUR-GEMINI-API-KEY" with your actual Gemini key in the .env file.

### ☁️ 2. Cloudinary Configuration — FixTrack/src/components/IssueForm.tsx

Replace or update the following constants in the IssueForm.tsx component:
```tsx
const CLOUD_NAME = 'YOUR-CLOUDINARY-CLOUD-NAME';
const UPLOAD_PRESET = 'YOUR-CLOUDINARY-UPLOAD-PRESET';
```
You can find these in your Cloudinary Console:
- Open your [Cloudinary Dashboard](https://cloudinary.com/console).
- Copy your Cloud Name and Upload Preset (or create a new preset under Settings → Upload).
- Replace the placeholders above with your actual credentials.

---

## 🗃️ Project Structure

```bash
FixTrack
├── public
│   ├── assets
│   ├── logo
│   │   ├── FixTrack.ico
│   │   └── FixTrack.png
│   ├── index.html
│   └── vite.svg
├── src
│   ├── animation
│   │   └── Map_Pinging.json
│   ├── components
│   │   ├── BuiltWith
│   │   │   ├── BuiltWith.css
│   │   │   └── BuiltWith.tsx
│   │   ├── ContactUs
│   │   │   ├── ContactUs.css
│   │   │   └── ContactUs.tsx
│   │   ├── Footer
│   │   │   ├── Footer.css
│   │   │   └── Footer.tsx
│   │   ├── Home
│   │   │   ├── Home.css
│   │   │   └── Home.tsx
│   │   ├── HowItWorks
│   │   │   ├── HowItWorks.css
│   │   │   └── HowItWorks.tsx
│   │   ├── LoadingSpinner
│   │   │   ├── LoadingSpinner.css
│   │   │   └── LoadingSpinner.tsx
│   │   ├── Navbar
│   │   │   ├── Navbar.css
│   │   │   └── Navbar.tsx
│   │   ├── OurTeam
│   │   │   ├── OurTeam.css
│   │   │   └── OurTeam.tsx
│   │   ├── Auth.css
│   │   ├── Auth.tsx
│   │   ├── Chatbot.css
│   │   ├── Chatbot.tsx
│   │   ├── Dashboard.css
│   │   ├── Dashboard.tsx
│   │   ├── IssueForm.css
│   │   ├── IssueForm.tsx
│   │   ├── IssueList.css
│   │   ├── IssueList.tsx
│   │   ├── Profile.css
│   │   ├── Profile.tsx
│   │   ├── ProfileMenu.css
│   │   ├── ProfileMenu.tsx
│   │   ├── UserManagement.css
│   │   └── UserManagement.css
│   ├── pages
│   │   ├── LandingPage.css
│   │   ├── LandingPage.test.tsx
│   │   └── LandingPage.tsx
│   ├── App.css
│   ├── App.tsx
│   ├── firebaseConfig.ts
│   ├── index.css
│   ├── main.tsx
│   ├── setupTests.ts
│   ├── types.ts
│   └── vite-env.d.ts
├── .env
├── .eslintrc.cjs
├── .firebaserc
├── cors.json
├── firebase.json
├── firebase.rules
├── index.html
├── package-lock.json
├── package.json
├── tsconfig.json
├── tsconfig.node.json
├── vite.config.ts
└── vitest.config.ts
```

---

## 🔥 Firebase Configuration

This project uses **Firebase** for backend services.  
To set it up:

1. Create a new project in the [Firebase Console](https://console.firebase.google.com/).
2. Add a new **web app** to your Firebase project.
3. Copy the Firebase configuration object.

---
 
## ⚙️ Firebase Deployment & Hosting

This project uses Firebase Hosting for deployment.
Below are the steps and commands used to configure, build, and deploy FixTrack from Firebase Studio:
```bash
# Log in to Firebase
firebase login

# Link your local project to a Firebase project
firebase use --add

# Initialize Firebase Hosting (select "dist" or your build folder)
firebase init hosting

# Build the production-ready project
npm run build

# Deploy to Firebase Hosting
firebase deploy --only hosting
```
After deployment, your production files will be available online via the Firebase Hosting URL.
The optimized build files are located in the dist directory.

---

<div align="center">

⭐ Love this project? Don’t forget to star it!

</div>
