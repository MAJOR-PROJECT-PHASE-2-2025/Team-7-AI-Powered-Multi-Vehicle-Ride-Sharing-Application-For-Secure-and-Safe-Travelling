🚗 Rydora – Real-World Ride-Sharing App

Rydora is a smart, real-world ride-sharing system designed to make urban commuting faster, safer, and cost-efficient.

Unlike normal apps, Rydora is modular and secure: the mobile apps are lightweight, and the core logic runs in a Python-based admin engine.

🌟 How Rydora Works – 3 Layers
1️⃣ Passenger App (Flutter + GraphHopper)

📱 Purpose: Allow passengers to request rides easily

⚡ Features:

Select pickup & destination

View route & fare

Request ride

🗺️ Tech: GraphHopper API for precise routing & fare calculation

2️⃣ Rider App (Flutter + OpenStreetMap)

🚖 Purpose: Allow drivers to accept and complete rides

⚡ Features:

Go online/offline 🟢/🔴

Live location updates every 5–10 seconds

Navigate using OpenStreetMap (cost-effective)

🗺️ Tech: OSM for continuous tracking

3️⃣ Python Admin Matcher (Jupyter Notebook)

🧠 Purpose: The “brain” of Rydora

⚡ Features:

Matches riders to passengers based on distance (Haversine formula)

Generates OTP for ride start 🔑

Admin controls: ban/unban drivers, verify users 👥

Analytics: ride density, peak hours 📊

System recovery after crashes 🔄

💡 Key Features & Advantages

🔒 Secure backend matching: Users cannot manipulate ride assignment

💰 Cost-efficient mapping: GraphHopper only for passengers, OSM for riders

⏱️ Real-time tracking: Firestore keeps everything updated instantly

🧪 Admin flexibility: Jupyter Notebook allows live monitoring and adjustments

🆔 OTP-based ride start: Ensures physical rider-passenger verification

🏗️ Scalable & modular: Easy to add AI features, surge pricing, pooling

🌍 Problems Rydora Solves

❌ Long wait times due to inefficient matching

❌ High cost of commercial map APIs

❌ Backend logic exposed in mobile apps

❌ No real-time admin controls

❌ Difficult to scale early-stage apps

Rydora solves this using a secure, cost-effective, and modular architecture.

🎯 Use Cases

🎓 College / Final-year project

🚀 Startup MVP

📱 System-design demo

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
