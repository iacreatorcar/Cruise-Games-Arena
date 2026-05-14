# 🚢 CRUISE GAMES ARENA

## Interactive Multi-Language Game System for Cruise Ships

### 📋 Overview

**Cruise Games Arena** is a real-time interactive quiz system designed for cruise ship entertainment. Passengers use their smartphones to participate, while the animator controls everything from a laptop with dual-screen support.

### 🎮 How It Works

#### For Passengers:
1. Scan QR code or open provided link
2. Register with:
   - Full Name
   - Cabin Number
   - Nationality
3. Select preferred language (ITA/ENG/FRA/DEU/ESP)
4. Answer 10 questions (one at a time)
5. Automatic logout after completion

#### For Animator:
- **Screen 1 (Public Display)**: Shows questions + live rankings
- **Screen 2 (Monitor)**: Real-time admin dashboard with:
  - Live participant tracking
  - Answer statistics
  - Provisional rankings
  - Export reports

### 🏆 Automatic Awards System

The system automatically determines:
- **1st Place** 🥇 (highest score, least errors, fastest time)
- **2nd Place** 🥈
- **3rd Place** 🥉

### 📊 Features

| Feature | Description |
|---------|-------------|
| 🌐 5 Languages | Italian, English, French, German, Spanish |
| 📱 No App Required | Works entirely in web browser |
| 🏅 Real-time Rankings | Live updates on public display |
| 📄 PDF Reports | One-click save/print results |
| 💾 Persistent Storage | Save data for future cruises |
| 🔄 Multiple Games | Easily add new game modules |

### 🛠️ Technical Requirements

- **Hosting**: Vercel (free) or any static web server
- **Database**: Firebase (free tier - 50k connections/day)
- **Internet**: Required for Firebase sync (or local WiFi network)
- **Devices**: Any device with modern web browser

### 🚀 Quick Start Guide

#### 1. Firebase Setup (5 minutes)

```bash
1. Go to https://console.firebase.google.com
2. Create new project: "cruise-games-arena"
3. Enable Authentication (Anonymous)
4. Create Realtime Database
5. Create Firestore Database
6. Get your Firebase config keys