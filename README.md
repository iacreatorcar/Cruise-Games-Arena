# 🚢 CRUISE GAMES ARENA

## 🏗️ System Architecture

```mermaid
graph TD
    A[🖥️ Admin Laptop] -->|Start Game| B[☁️ Firebase]
    B -->|Status: active| C[📺 Public Display]
    D[📱 Passenger Phone] -->|Scan QR| E[📝 Register]
    E -->|Submit Answers| B
    B -->|Real-time scores| C
    B -->|Live stats| A
    C -->|Show rankings| F[📺 TV Screen]
    F -->|Live leaderboard| D
🔄 Data Flow
Step    Action
1    Animator starts game → Firebase status = active
2    Passengers scan QR → register with name, cabin, nationality
3    Passengers answer questions → scores saved to Firebase
4    Firebase syncs real-time → TV shows live rankings
5    All players complete → system calculates winners automatically
📊 Real-time Performance
Metric    Value
Registration time    < 1 second
Answer submission    < 1 second
Rankings update    < 1 second
Concurrent players    100+

