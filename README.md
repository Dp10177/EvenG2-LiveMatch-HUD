📊 LiveMatch HUD – Even G2 Real-Time Scoreboard
LiveMatch HUD transforms your Even G2 smart glasses into a real-time sports overlay. Track live matches, view accurate match timing, and access detailed statistics — all directly in your field of vision.
🚀 Features
⚽ Live scoreboard overlay (TV-style)
⏱ Real-time match clock (high precision)
📊 Detailed stats (shots, fouls, possession, cards, corners)
📱 Multi-match selection menu
🧠 Lightweight AR-optimized interface
🔄 Real-time sync via WebSockets
🧱 Architecture

Even G2 (HUD)
   ↓
WebView (Frontend UI)
   ↓
WebSocket (Realtime Sync)
   ↓
Node.js Backend
   ↓
Sports Data API (API-Football / Sportmonks)
📁 Project Structure

g2-livematch-hud/
│
├── frontend/        # HUD interface
├── backend/         # WebSocket server + API sync
├── even-plugin/     # Even Hub plugin config
├── package.json
└── README.md
⚙️ Setup
1. Clone the repo
Bash
git clone https://github.com/yourusername/g2-livematch-hud.git
cd g2-livematch-hud
2. Install dependencies
Bash
npm install
3. Add API Key
Edit:

backend/sportsApi.js
Replace:
JavaScript
const API_KEY = "YOUR_API_KEY";
4. Run backend
Bash
node backend/server.js
5. Run frontend
Use any dev server (Vite recommended):
Bash
npm run dev
🔌 Even Hub Integration
Package the even-plugin folder
Upload to Even Hub
Ensure WebView points to your frontend URL:
JavaScript
display.openWebView("http://localhost:5173");
⚡ Real-Time Engine
WebSocket updates every 200ms–1000ms
Live match syncing via external sports APIs
Supports multiple simultaneous matches
🔮 Roadmap
🎨 Advanced UI themes (Champions League style)
🔔 Goal alerts & notifications
📡 Multi-sport support (NBA, UFC, etc.)
🧠 AI insights (xG, predictions)
🎙 Voice commands integration
⚠️ Notes
No official LiveScore API is used
Data provided via third-party APIs (API-Football, etc.)
Even Hub SDK is currently limited → WebView approach used
📄 License
MIT License
👨‍💻 Author
Built for Even G2 developers pushing AR experiences forward.
