# CreatorHub - Content Creator Social Media Dashboard

CreatorHub is a high-performance single-dashboard web application designed for social media content creators, matching modern dark-mode aesthetic standards with vibrant accent pill badges and responsive UI layout.

---

## 🌟 Core Features

1. **Dashboard Overview**:
   - 4 Top Cards: Total Views (`2.4M`), Total Earnings (`$12,458`), Videos in Folder (`48`), Languages Count (`9`).
   - Recent Videos Table with video thumbnails, language tags (Hindi, Tamil, English, etc.), publish dates, views count, estimated earnings, and visibility toggle (`Public`/`Private`).
2. **Video & Photo Management**:
   - Photo Upload & Gallery grid view.
   - Video Upload with title, language selection, category, and automatic earnings calculation (`views * $0.005`).
3. **Earnings & Monetization**:
   - Estimated earnings calculator and payout status tracking.
   - Interactive line graphs and revenue breakdown bar charts using Chart.js.
4. **Real-time Messaging**:
   - Real-time chat inbox with active thread messaging powered by Firebase Firestore / instant local stream simulation.
5. **1-on-1 WebRTC Video & Audio Calls**:
   - Built-in PeerJS WebRTC video and audio calling with camera/mic controls.
6. **Firebase Integration & Demo Fallback**:
   - Zero-config **Instant Demo Mode** pre-loaded with realistic reference data so it works immediately out-of-the-box.
   - Single configuration file `js/firebase-config.js` for live Firebase Auth, Firestore, and Storage integration.

---

## 🚀 Quick Start (Local Development)

### 1. Install Dependencies
```bash
npm install
```

### 2. Run Local Development Server
```bash
npm run dev
```
Open your browser at `http://localhost:5173`.

---

## 🔥 Firebase Configuration Guide (Optional for Live Mode)

To connect CreatorHub to your live Firebase backend:

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. Enable **Authentication** (Email/Password), **Cloud Firestore**, and **Firebase Storage**.
3. Open `js/firebase-config.js` in your codebase and paste your project config keys:

```javascript
export const firebaseConfig = {
  apiKey: "YOUR_FIREBASE_API_KEY",
  authDomain: "your-app.firebaseapp.com",
  projectId: "your-app-id",
  storageBucket: "your-app.appspot.com",
  messagingSenderId: "1234567890",
  appId: "1:1234567890:web:abcdef123456"
};
```
CreatorHub will automatically detect your keys and connect to your live Firebase backend!

---

## 🌐 Free Hosting & Deployment (Single Command)

### Option A: Deploy Free on Vercel (Recommended)
Run the following single command in your terminal:
```bash
npx vercel --prod
```
Follow the quick prompts in your shell, and your live URL will be generated instantly.

### Option B: Deploy Free on Netlify
```bash
npx netlify deploy --prod
```

### Option C: Deploy Free on Firebase Hosting
```bash
npx firebase-tools login
npx firebase-tools init hosting
npx firebase-tools deploy
```

---

## 🛠 Tech Stack
- **Frontend**: HTML5, CSS3 (Vanilla Dark Design Tokens), ES Modules JavaScript
- **Build Tool**: Vite (Lightning fast static builder)
- **Charts**: Chart.js v4
- **WebRTC Calls**: PeerJS
- **Backend & Storage**: Firebase v10 (Auth, Firestore, Storage)
