Rydora is a complete ride-sharing system designed for real-world urban mobility, combining cost efficiency, security, and scalability. Unlike typical apps where all logic is inside the mobile app, Rydora separates responsibilities into three layers:

Passenger App (Flutter + GraphHopper)

Lightweight mobile client

Allows passengers to:

Select pickup & destination

View route and fare

Request rides

Uses GraphHopper API for precise routing and fare estimation

Rider App (Flutter + OpenStreetMap)

Lightweight driver client

Features:

Go online/offline

Live location tracking (heartbeat every 5–10 seconds)

Navigation using OpenStreetMap (cost-free alternative to Google Maps)

Sends updates to Firestore so the admin engine can match riders to passengers

Python Admin Matcher (Jupyter Notebook)

Core backend engine and admin dashboard

Responsibilities:

Match ride requests to nearest available riders

Generate OTP for ride start (prevents fake rides)

Admin controls (ban/unban users, verify drivers)

Analytics (ride density, peak-hour trends)

System recovery (reset stuck rides, clear inactive drivers)

Key Features & Advantages:

Secure backend matching: Riders and passengers cannot manipulate assignment logic

Cost-optimized mapping: Uses OSM for frequent driver updates, GraphHopper for precise passenger routing

Real-time tracking: Firestore enables live state synchronization

Admin control & analytics: Jupyter Notebook allows live code execution for system monitoring

OTP-based ride start: Verifies physical rider-passenger presence

Scalable & modular: Easy to extend (AI demand prediction, surge pricing, ride pooling)

Problem Solved:

Eliminates inefficiencies in ride matching

Reduces dependency on expensive map APIs

Provides admin flexibility for real-time control and analytics

Makes a secure, startup-friendly, and production-like ride-sharing solution

Use Cases:

College / final-year project

Startup MVP

System-design portfolio

Demonstrates backend + distributed system concepts

Perfect 👍
Below is a **ready-to-use README section** that **fully satisfies evaluation / placement / GitHub guidelines**.

You can **copy-paste this directly** into each Rydora repository
(Passenger App / Rider App / Admin Matcher), with **small edits per repo**.

---

# 📘 README.md – Mandatory Project Documentation

## 🚀 Steps to Run the Project

### 1️⃣ Prerequisites

Ensure the following are installed:

* Flutter SDK (latest stable)
* Python 3.10+
* Firebase account & project
* Jupyter Notebook / Jupyter Lab
* Git

---

### 2️⃣ Clone the Repository

```bash
git clone https://github.com/ChandanM123456/Rydora-Ride-Sharing-App-for-Real-World-Urban-Mobility
cd Rydora-Ride-Sharing-App-for-Real-World-Urban-Mobility
```

---

### 3️⃣ Firebase Setup

1. Create a Firebase project
2. Enable **Firestore Database**
3. Download configuration files:

   * `google-services.json` → `android/app/`
   * `GoogleService-Info.plist` → `ios/Runner/`
4. Create collections:

   * `ride_requests`
   * `active_riders`
   * `historical_rides`

---

### 4️⃣ Run Passenger App

```bash
cd rydora_passenger
flutter pub get
flutter run
```

📍 Enter pickup & destination
💰 View route and fare
🚕 Request a ride

---

### 5️⃣ Run Rider App

```bash
cd rydora_rider
flutter pub get
flutter run
```

🚗 Login as rider
🟢 Toggle **Go Online**
📡 Location updates sent to Firestore

---

### 6️⃣ Run Python Admin Matcher

```bash
cd admin_matcher
pip install firebase-admin pandas matplotlib ipywidgets
jupyter lab
```

* Open `admin_matcher.ipynb`
* Run initialization cell
* Run matching loop cell

🧠 Ride matching starts automatically

---

## 📸 Project Snapshots / Screenshots

> Add screenshots inside a `/screenshots` folder

### 📱 Passenger App

* Home Screen
* Route & Fare Preview
* Ride Request Confirmation

### 🚖 Rider App

* Rider Dashboard
* Live Navigation Map
* OTP Ride Start Screen

### 🧠 Admin Matcher

* Jupyter Matching Logs
* Ride Analytics Graphs

```md
![Passenger Home](screenshots/passenger_home.png)
![Rider Map](screenshots/rider_map.png)
![Admin Analytics](screenshots/admin_analytics.png)
```

---

## 🎥 Demo Video

📽️ **Project Demo Video Link:**
👉 [https://drive.google.com/your-demo-video-link](https://drive.google.com/your-demo-video-link)

**Demo covers:**

* Passenger requesting a ride
* Rider going online
* Admin matching process
* OTP-based ride start
* Ride completion

> ⚠️ *Mandatory for evaluation – ensure video is accessible*

---

## 🛠️ Technologies Used

### 📱 Frontend (Mobile Apps)

* Flutter
* Dart
* flutter_map
* OpenStreetMap (OSM)

### 🗺️ Mapping & Routing

* GraphHopper API (Passenger)
* OpenStreetMap Tiles (Rider)

### 🔥 Backend & Realtime Sync

* Firebase Firestore
* Firebase Authentication

### 🧠 Logic & Admin Layer

* Python 3.10+
* Firebase Admin SDK
* Jupyter Notebook
* Pandas
* Matplotlib

### 🔐 Security

* Firestore Security Rules
* OTP-based ride verification
* Service Account authentication

---

## ✅ Evaluation Checklist (Tick All)

✔ Steps to run clearly documented
✔ Screenshots included
✔ Demo video link provided
✔ Technologies explicitly listed
✔ Real-world problem addressed
✔ Modular & scalable architecture

---

## 👤 Author

**Chandan M**
📧 [chandan.chandu0608@gmail.com](mailto:chandan.chandu0608@gmail.com)
