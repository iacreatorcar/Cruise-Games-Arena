# 🚢 CRUISE GAMES ARENA

## Professional Interactive Quiz System for Cruise Ships

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/)
[![Firebase](https://img.shields.io/badge/Firebase-9.22-orange.svg)](https://firebase.google.com/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

---

## 📋 Overview

**Cruise Games Arena** is a real-time, multi-language interactive quiz system designed specifically for cruise ship entertainment. Passengers use their smartphones to participate, while the animator controls everything from a laptop with dual-screen support.

### ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🎮 **Real-time Gameplay** | Instant updates as players answer questions |
| 🌐 **5 Languages** | English, Italian, French, German, Spanish |
| 📱 **No App Required** | Works entirely in web browser |
| 🏆 **Live Rankings** | Real-time leaderboard on public display |
| 🖨️ **PDF Reports** | One-click save/print results |
| 📊 **CSV Export** | Complete player data export |
| 🔄 **Multiple Games** | Easily add new quiz modules via JSON |
| 🎯 **Game Control** | Start/Pause/Stop from admin panel |

---

## 🎮 How It Works

### For Passengers:
1. Scan QR code or open provided link
2. Register with:
   - Full Name
   - Cabin Number
   - Nationality
3. Select preferred language
4. Answer questions (one at a time)
5. Automatic logout after completion

### For Animator:
- **Screen 1 (Public Display)**: Shows questions + live rankings
- **Screen 2 (Monitor)**: Real-time admin dashboard

### For Technical Manager:
- Full control panel to start/stop games
- Load custom quizzes via JSON
- Export results and print reports
- Monitor player statistics in real-time

---

## 🏆 Automatic Awards System

The system automatically determines:
- 🥇 **1st Place** (highest score, least errors)
- 🥈 **2nd Place**
- 🥉 **3rd Place**

---

## 📂 Project Structure
cruise-games-arena/
├── index.html # Player interface (mobile)
├── screen.html # Public display (TV/projector)
├── admin-panel.html # Technical admin panel
├── start-here.html # Professional launcher hub
├── style.css # Global styles
├── firebase-config.js # Firebase configuration (local only)
├── games/ # Game JSON files
│ ├── cruise_quiz.json
│ ├── destinations.json
│ ├── culture.json
│ ├── cinema.json
│ ├── music.json
│ └── sports.json
└── README.md # This documentation

text

---

## 🛠️ Technical Requirements

| Requirement | Specification |
|-------------|---------------|
| **Hosting** | Vercel (free) or any static web server |
| **Database** | Firebase (free tier - 50k connections/day) |
| **Internet** | Required for Firebase sync (or local WiFi network) |
| **Devices** | Any device with modern web browser |

### Firebase Free Tier Limits (sufficient for cruise ships):
- 50,000 reads/day
- 20,000 writes/day
- 100 simultaneous connections
- 1 GB storage

---

## 🚀 Quick Start Guide

### 1. Firebase Setup (5 minutes)

```bash
1. Go to https://console.firebase.google.com
2. Create new project: "cruise-games-arena"
3. Enable Firestore Database (Test mode)
4. Go to Project Settings → Your apps → Web (</>)
5. Copy your Firebase configuration keys
2. Configure Firebase
Create firebase-config.js in project root:

javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "cruise-games-arena.firebaseapp.com",
    projectId: "cruise-games-arena",
    storageBucket: "cruise-games-arena.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};

firebase.initializeApp(firebaseConfig);
const db = firebase.firestore();
window.db = db;
3. Run Locally
bash
# Using Python
python -m http.server 3000

# Using Node.js
npx http-server 3000

# Using VS Code Live Server
Right-click index.html → Open with Live Server
4. Deploy to Vercel (Free)
bash
1. Push code to GitHub repository
2. Go to https://vercel.com
3. Import GitHub repository
4. Deploy (no configuration needed)
📱 Usage Instructions
For Animator / Technical Manager:
Start the server and open start-here.html

Click Technical Admin → START GAME

Display QR code for passengers

Monitor live statistics

Click Next Question on public display

Export results when game ends

For Passengers:
Scan QR code with phone camera

Enter your details:

text
Name: John Smith
Cabin: 1234
Nationality: United Kingdom
Select language

Answer questions

Watch public screen for rankings!

📊 Game JSON Format
Create custom quizzes with this format:

json
{
  "name": "Game Title",
  "questions": [
    {
      "text": "Question text?",
      "options": ["Option A", "Option B", "Option C", "Option D"],
      "correct": 0
    }
  ]
}
Note: correct is 0-indexed (0=A, 1=B, 2=C, 3=D)

🎯 Included Games
Game	File	Questions
🚢 Cruise Quiz 2024	cruise_quiz.json	10
🏝️ Destination Challenge	destinations.json	10
📚 General Culture	culture.json	10
🎬 Cinema & TV	cinema.json	10
🎵 Music Trivia	music.json	10
⚽ Sports Quiz	sports.json	10
🖨️ Reports & Export
PDF Report
Click Print Report in admin panel → Save as PDF

CSV Export
Click Export CSV → Download complete player data:

csv
Position,Name,Cabin,Nationality,Score,Errors,Status
1,John Smith,1234,United Kingdom,10,0,Completed
2,Marie Curie,5678,France,9,1,Completed
🔧 Troubleshooting
Issue	Solution
Players can't connect	Check WiFi network; ensure same subnet (192.168.1.x)
Firebase errors	Verify firebase-config.js has correct keys
Blank pages	Clear browser cache (Ctrl+Shift+R)
QR code not working	Use IP address, not localhost
Slow updates	Check Firebase quota usage
📈 System Architecture
text
┌─────────────────────────────────────────────────────────┐
│                    CRUISE SHIP NETWORK                   │
├─────────────────────────────────────────────────────────┤
│                                                          │
│  ┌──────────────┐     ┌──────────────┐                  │
│  │   LAPTOP     │     │   TV SCREEN  │                  │
│  │ (Animator)   │     │ (Public)     │                  │
│  │              │     │              │                  │
│  │ Admin Panel  │────▶│  Display     │                  │
│  │ Start/Stop   │     │  Live Scores │                  │
│  └──────┬───────┘     └──────────────┘                  │
│         │                                                │
│         ▼                                                │
│  ┌──────────────┐     ┌──────────────┐                  │
│  │   FIREBASE   │     │   PASSENGERS │                  │
│  │   Cloud DB   │◀───▶│ (Smartphones)│                  │
│  │  Real-time   │     │              │                  │
│  └──────────────┘     │  Play Game   │                  │
│                       └──────────────┘                  │
└─────────────────────────────────────────────────────────┘
🔐 Security Notes
firebase-config.js is excluded from Git (add to .gitignore)

Use Firebase Security Rules in production

Change API keys if compromised

Never commit .env files

📄 License
MIT License - Free for commercial use on cruise ships

👨‍💻 Support
For technical support:

Email: support@cruisegamesarena.com

Documentation: This README

GitHub Issues: Create an issue in the repository

🏆 Version History
Version	Date	Changes
v1.0.0	2024	Initial release
Multi-language support
Real-time ranking system
PDF/CSV export
6 pre-built games
🚢 Final Notes
Cruise Games Arena transforms any cruise ship into an interactive entertainment hub. With no app installation required, passengers simply scan and play, while the crew maintains full control from a simple dashboard.

Made with ❤️ for unforgettable cruise experiences

For best results, test the system before each cruise and ensure all devices are on the same WiFi network.

text

---

## ✅ **File Summary**

| File | Purpose |
|------|---------|
| `start-here.html` | Professional launcher hub with QR generation |
| `README.md` | Complete documentation for developers and operators |

---

## 🚀 **How to Use**

1. Save `start-here.html` in your project root
2. Save `README.md` in your project root
3. Open `start-here.html` in browser when server is running
4. Share the README with your team

## 👨‍💻 Contact & Support

**Founder & Developer:** Carmine D'Alise

📧 **Email:** [carmine@cdalise.com](mailto:carmine@cdalise.com)

🔗 **GitHub:** [github.com/iacreatorcar](https://github.com/iacreatorcar)

🌐 **Website:** [cdalise.com](https://cdalise.com)

---

*For commercial inquiries, cruise ship installations, or custom development, feel free to reach out.*
---

**Now you have a complete professional package!** 🚢