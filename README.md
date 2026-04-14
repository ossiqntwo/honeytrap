🍯 HoneyTrap Network

Advanced Honeypot & Threat Intelligence System
Developed & Maintained by ossiqn

🔍 What is HoneyTrap Network?

HoneyTrap Network is a fully automated honeypot system that:

Lures attackers into fake services
Captures everything they do
Reports activity in real time

All data is visualized through a sleek dark-themed web dashboard and sent instantly via Discord and Telegram.

Deploy it → Watch attackers walk in → Collect intelligence automatically

✨ Features
Feature	Description
🌐 HTTP Trap	Fake APIs, admin panels, .env, phpMyAdmin, WordPress login, GraphQL
🔐 SSH Trap	Captures brute-force attempts and executed commands
📁 FTP Trap	Fake files, credential logging, download tracking
🔌 TCP Trap	Emulates MySQL, PostgreSQL, Redis, MongoDB, Elasticsearch, Jupyter
🌍 GeoIP	Real-time attacker location (country, city, ISP, ASN)
🧬 IOC Export	Automatically generates IOC lists
🗺️ Attack Map	Visual global attack tracking
🔥 Threat Score	Automatic scoring based on attacker behavior
🚫 Auto Blacklist	Blocks high-risk IPs automatically
💬 Discord Alerts	Real-time webhook notifications
📱 Telegram Alerts	Instant bot alerts
🖥️ Web Dashboard	Live terminal-style UI with CRT effect
🐳 Docker Ready	One-command deployment
📊 SQLite DB	Local storage of attacks and sessions
🚀 Quick Start
🐳 Docker (Recommended)
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

Fake endpoints that mimic real services:

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
🔍 Advanced Filtering
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
Backend: Python 3.11+
Web: Flask
SSH: Paramiko
Database: SQLite + SQLAlchemy
GeoIP: ip-api.com
Notifications: Discord Webhook + Telegram Bot
Frontend: Vanilla JS + CSS3
Container: Docker + Docker Compose
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

❌ Not allowed:

Unauthorized deployment on external systems

Unauthorized use may violate cybercrime laws.

👤 Developer
Name: ossiqn
Website: ossiqn.com.tr
GitHub: github.com/ossiqn
📜 License

MIT License — © 2024 ossiqn
