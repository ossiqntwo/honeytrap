# 🍯 HoneyTrap Network
### Advanced Honeypot & Threat Intelligence System  
**Developed & Maintained by ossiqn**

---

## 🔍 What is HoneyTrap Network?

HoneyTrap Network is a fully automated honeypot system that:

- Lures attackers into fake services  
- Captures everything they do  
- Reports activity in real time  

All data is visualized through a sleek dark-themed web dashboard and sent instantly via Discord and Telegram.

> **Deploy it → Watch attackers walk in → Collect intelligence automatically**

---

## ✨ Features

- 🌐 **HTTP Trap** — Fake APIs, admin panels, `.env`, phpMyAdmin, WordPress, GraphQL  
- 🔐 **SSH Trap** — Captures brute-force attempts and executed commands  
- 📁 **FTP Trap** — Logs credentials and file downloads  
- 🔌 **TCP Trap** — Emulates DBs and services (MySQL, Redis, MongoDB, etc.)  
- 🌍 **GeoIP** — Real-time attacker geolocation  
- 🧬 **IOC Export** — Auto-generates IOC lists  
- 🗺️ **Attack Map** — Visual global attack tracking  
- 🔥 **Threat Score** — Automatic attacker scoring  
- 🚫 **Auto Blacklist** — Blocks malicious IPs  
- 💬 **Discord Alerts** — Real-time notifications  
- 📱 **Telegram Alerts** — Instant alerts  
- 🖥️ **Web Dashboard** — Live terminal-style UI  
- 🐳 **Docker Ready** — One-command deployment  
- 📊 **SQLite DB** — Local storage  

---

## 🚀 Quick Start

### 🐳 Docker (Recommended)

```bash
git clone https://github.com/ossiqn/honeytrap
cd honeytrap
cp .env.example .env
nano .env
docker-compose up -d
🛠️ Manual Installation
git clone https://github.com/ossiqn/honeytrap
cd honeytrap
pip install -r requirements.txt
cp .env.example .env
python src/main.py
🌐 Web Dashboard
http://localhost:5000
⚙️ Configuration (.env)
DISCORD_WEBHOOK_URL=https://discord.com/api/webhooks/...
TELEGRAM_BOT_TOKEN=1234567890:AAxxxxxxxxx
TELEGRAM_CHAT_ID=-1001234567890
🪤 Trap Details
🌐 HTTP Trap (:8080)
/api/login     → Captures credentials, returns fake JWT
/api/admin     → Fake admin panel
/api/config    → Fake AWS keys, DB credentials
/.env          → Fake environment file
/wp-admin      → Fake WordPress login
/phpmyadmin    → Fake phpMyAdmin
/graphql       → Fake GraphQL schema
/shell         → Logs RCE attempts
/backup        → Fake download trigger
🔐 SSH Trap (:2222)
Logs all login attempts (username/password)
Records executed commands
Returns realistic shell responses
📁 FTP Trap (:2121)
Lists fake sensitive files
Captures login credentials
Logs download attempts
🔌 TCP Traps
3306  → MySQL
5432  → PostgreSQL
6379  → Redis
27017 → MongoDB
9200  → Elasticsearch
8888  → Jupyter
4444  → Backdoor listener
📊 Web Dashboard Features
⚡ Live Attack Feed
🧬 IOC List
🗺️ Attack Map
🚫 Blacklist Manager
🔍 Filter by Trap / Severity
📤 Export as JSON
🔔 Notification Example (Discord)
🔴 SSH TRAP — CRITICAL
━━━━━━━━━━━━━━━━━━━━━━━
🎯 Severity : CRITICAL
🪤 Trap     : SSH
🌍 Country  : Russia
🖥️ IP       : 185.xxx.xxx.xxx
🔥 Score    : 85/100
🔒 VPN      : YES
👤 Username : root
🔑 Password : toor123
🛠️ Tech Stack
Python 3.11+
Flask
Paramiko
SQLite + SQLAlchemy
ip-api.com
Discord Webhook + Telegram Bot
Vanilla JS + CSS3
Docker + Docker Compose
📁 Project Structure
honeytrap/
├── src/
│   ├── main.py
│   ├── traps/
│   │   ├── http_trap.py
│   │   ├── ssh_trap.py
│   │   ├── ftp_trap.py
│   │   └── tcp_trap.py
│   ├── core/
│   │   ├── db.py
│   │   ├── geoip.py
│   │   └── ioc.py
│   ├── notifier/
│   │   ├── discord.py
│   │   └── telegram.py
│   └── web/
│       ├── app.py
│       ├── templates/
│       └── static/
├── config.yml
├── docker-compose.yml
└── requirements.txt
⚠️ Legal Disclaimer

This tool is intended for defensive security research only.

✅ Allowed:
Systems you own
Authorized penetration testing
Threat intelligence research
Educational use
❌ Not Allowed:
Unauthorized deployment on external systems

Misuse may violate local and international laws.

👤 Developer
🌐 Website: https://ossiqn.com.tr
🐙 GitHub: https://github.com/ossiqn
📜 License

MIT License — © 2024 ossiqn

⭐ If you like this project, consider giving it a star!
