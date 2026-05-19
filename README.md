<!-- 
  CRUISE GAMES ARENA
  Professional Interactive Quiz System for Cruise Ships
  Version: 1.0.0 | Author: Carmine D'Alise
-->

<div align="center">

# 🚢 CRUISE GAMES ARENA

### Real-time Interactive Quiz System for Cruise Ships

[![Live Demo](https://img.shields.io/badge/Live_Demo-vercel.app-brightgreen?style=for-the-badge&logo=vercel)](https://cruise-games-arena.vercel.app)
[![Made with Firebase](https://img.shields.io/badge/Made_with-Firebase-orange?style=for-the-badge&logo=firebase)](https://firebase.google.com)
[![License MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](http://makeapullrequest.com)

<br>

<img src="assets/dashboard.png" width="800" alt="Cruise Games Arena Dashboard" style="border-radius: 20px; border: 1px solid #333; box-shadow: 0 10px 30px rgba(0,0,0,0.3);">

</div>

---

## 📋 Table of Contents

- [What is Cruise Games Arena?](#what-is-cruise-games-arena)
- [Key Features](#key-features)
- [How It Works](#how-it-works)
- [System Architecture](#system-architecture)
- [Screenshots](#screenshots)
- [Live Demo](#live-demo)
- [Use Cases](#use-cases)
- [Included Games](#included-games)
- [Technology Stack](#technology-stack)
- [Quick Start](#quick-start)
- [Contact](#contact)

---

## 🎯 What is Cruise Games Arena?

**Cruise Games Arena** is a professional, real-time quiz system designed for cruise ship entertainment, resorts, hotels, and corporate events. 

Passengers play from their smartphones with **no app installation required**, while the crew controls everything from a simple, intuitive dashboard.

### Built For:

- ✅ Cruise ships & ferries
- ✅ Beach resorts & hotels
- ✅ Corporate events & team building
- ✅ Large-scale entertainment venues

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🎮 **Real-time Gameplay** | Instant scoring and live rankings |
| 🌐 **5 Languages** | English, Italian, French, German, Spanish |
| 📱 **No App Required** | Works entirely in web browser |
| 🏆 **Live Rankings** | Real-time leaderboard on public display |
| 🖨️ **PDF & CSV Reports** | One-click export of results |
| 🔄 **Multiple Games** | Easily add new quizzes via JSON |
| 🎯 **Game Control** | Start/Pause/Stop from admin panel |
| 👥 **Player Management** | Track names, cabins, nationalities |
| ⏱️ **Auto/Manual Mode** | 10-second timer or host-controlled |

---

## 🎮 How It Works

<div align="center">

| Step | Action |
|:----:|--------|
| 1️⃣ | **Host/Animator** selects a game and clicks **START** |
| 2️⃣ | **Passengers** scan QR code with their phone |
| 3️⃣ | **Register** with Name, Cabin, Nationality |
| 4️⃣ | **Answer** questions (10 per game) |
| 5️⃣ | **Live rankings** appear on public screen |
| 6️⃣ | **Winners** are automatically announced |

</div>

### 👥 User Roles

| Role | Interface | Actions |
|------|-----------|---------|
| 🎮 **Passenger** | Mobile browser | Register, answer questions, view score |
| 📺 **Public Display** | TV/LED wall | Show questions, live rankings, winners |
| 🖥️ **Animator** | Laptop (admin panel) | Start/stop game, manage questions, export results |
| 🔧 **Technical Admin** | Laptop (full control) | Game selection, player management, database cleanup |

---

## 🏗️ System Architecture
┌─────────────────────────────────────────────────────────────────┐
│ CRUISE SHIP NETWORK │
├─────────────────────────────────────────────────────────────────┤
│ │
│ ┌──────────────┐ ┌──────────────┐ │
│ │ LAPTOP │ │ TV SCREEN │ │
│ │ (Animator) │ │ (Public) │ │
│ │ │ │ │ │
│ │ Admin Panel │─────────────────────▶│ Live Scores │ │
│ │ Start/Stop │ │ Rankings │ │
│ └──────┬───────┘ └───────────────┘ │
│ │ │
│ ▼ │
│ ┌──────────────┐ ┌──────────────┐ │
│ │ FIREBASE │◀────────────────────▶│ PASSENGERS │ │
│ │ Cloud DB │ │ (Smartphones) │ │
│ │ Real-time │ │ │ │
│ └──────────────┘ │ Play Game │ │
│ └───────────────┘ │
│ │
└─────────────────────────────────────────────────────────────────┘

### 🔄 Data Flow

1. **Animator** starts the game via Admin Panel
2. **Firebase** updates game state to `active`
3. **Passengers** scan QR and register
4. **Answers** are saved in real-time to Firebase
5. **Public Display** shows live rankings
6. **Winners** are automatically calculated
7. **Reports** can be exported as CSV or PDF

---

## 🖼️ Screenshots

<div align="center">

| Admin Dashboard | Public Display | Player View |
|:---:|:---:|:---:|
| <img src="assets/screenshots/admin-thumb.png" width="300" alt="Admin Dashboard"> | <img src="assets/screenshots/display-thumb.png" width="300" alt="Public Display"> | <img src="assets/screenshots/player-thumb.png" width="300" alt="Player View"> |
| *Full control panel* | *Live rankings & questions* | *Mobile registration* |

</div>

### 📋 Features shown in screenshots:

| Screenshot | Features |
|------------|----------|
| **Admin Dashboard** | Game controls, live statistics, player ranking, game selector, export buttons |
| **Public Display** | Current question, live rankings, timer, winner podium |
| **Player View** | Registration form, quiz interface, multi-language support |

---

## 🚀 Live Demo

👉 **Try it yourself:** [https://cruise-games-arena.vercel.app](https://cruise-games-arena.vercel.app)

📱 **Scan QR to play:**

<div align="center">
  <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://cruise-games-arena.vercel.app/start-here.html" width="150">
  <br>
  <i>Scan with your phone camera</i>
</div>

---

## 🎯 Use Cases

| Industry | Application |
|----------|-------------|
| 🚢 **Cruise Ships** | Main entertainment activity, evening quizzes |
| 🏖️ **Resorts** | Poolside games, family activities |
| 🏨 **Hotels** | Guest engagement, welcome events |
| 🎪 **Corporate Events** | Team building, conference icebreakers |
| 🎓 **Education** | Interactive learning, student engagement |

---

## 📦 Included Games

| Game | Questions | Difficulty | Theme |
|------|-----------|------------|-------|
| 🚢 Cruise Quiz 2024 | 10 | Medium | Nautical trivia |
| 🌍 Geography Challenge | 10 | Hard | World geography |
| 📜 History Trivia | 10 | Medium | Historical facts |
| 🏝️ Destination Challenge | 10 | Easy | Travel destinations |
| 🎬 Cinema & TV | 10 | Medium | Movies & series |
| 🎵 Music Trivia | 10 | Easy | Pop culture |
| ⚽ Sports Quiz | 10 | Medium | Global sports |

---

## 🛠️ Technology Stack

<div align="center">

| Layer | Technology |
|:-----:|:----------:|
| **Frontend** | HTML5, CSS3, JavaScript (ES6+) |
| **Backend** | Firebase Firestore (Real-time DB) |
| **Hosting** | Vercel / GitHub Pages |
| **QR Code** | QR Server API |
| **Version Control** | Git & GitHub |

</div>

### 📊 Firebase Free Tier Limits

| Resource | Limit |
|----------|-------|
| Reads/day | 50,000 |
| Writes/day | 20,000 |
| Simultaneous connections | 100 |
| Storage | 1 GB |

*Sufficient for a cruise ship with 100+ passengers*

---

## 🚀 Quick Start

### Prerequisites

- Node.js (optional, for local server)
- Firebase account (free)
- Git (for version control)

### 1. Clone the repository

```bash
git clone https://github.com/iacreatorcar/Cruise-Games-Arena.git
cd Cruise-Games-Arena### 2. Install dependencies

