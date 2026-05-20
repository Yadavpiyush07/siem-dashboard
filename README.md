```ruby
███████╗██╗███████╗███╗   ███╗
██╔════╝██║██╔════╝████╗ ████║
███████╗██║█████╗  ██╔████╔██║
╚════██║██║██╔══╝  ██║╚██╔╝██║
███████║██║███████╗██║ ╚═╝ ██║
╚══════╝╚═╝╚══════╝╚═╝     ╚═╝
```

> Full-stack SIEM dashboard with real-time log correlation, alert management, and attack simulation inspired by modern SOC platforms.

This project is built for learning SIEM architecture, SOC workflows, detection engineering, and security event monitoring using a modern full-stack setup.

------------------------------------------------------------
WHAT THIS PROJECT DOES
------------------------------------------------------------

This project simulates a lightweight SIEM (Security Information and Event Management) platform similar to:

- Splunk
- QRadar
- Elastic SIEM
- Microsoft Sentinel

The platform allows you to:

- Monitor security logs in real time
- Generate and correlate security events
- Simulate cyber attacks using predefined scenarios
- Trigger alerts based on detection rules
- Visualize incidents inside a dashboard
- Practice SOC analyst workflows locally

------------------------------------------------------------
FEATURES
------------------------------------------------------------

- Real-time log ingestion and event correlation
- Security alert generation and management
- MITRE ATT&CK inspired attack simulations
- Dashboard for monitoring security events
- Live alert feeds using Server-Sent Events (SSE)
- Multiple correlation rule types:
  - Threshold rules
  - Sequence rules
  - Aggregation rules
- Attack playbooks written in YAML
- Alert lifecycle management:
  - Acknowledge
  - Investigate
  - Resolve
  - False Positive
- Docker-based deployment for easy setup

------------------------------------------------------------
ATTACK SIMULATIONS INCLUDED
------------------------------------------------------------

The project can simulate:

- SSH Brute Force Attacks
- DNS Tunneling
- Phishing Activity
- Privilege Escalation
- Suspicious Login Attempts
- Multi-stage Attack Chains

------------------------------------------------------------
TECH STACK
------------------------------------------------------------

Backend:
- Flask
- MongoEngine
- Redis Streams
- Pydantic
- JWT Authentication
- Gunicorn

Frontend:
- React 19
- TypeScript
- Vite
- Zustand
- TanStack Query
- SCSS Modules

Database & Infrastructure:
- MongoDB 8
- Redis 7
- Docker Compose
- Nginx

------------------------------------------------------------
PROJECT STRUCTURE
------------------------------------------------------------

backend/        → Flask API & correlation engine
frontend/       → React dashboard UI
conf/           → Nginx and configuration files
learn/          → Learning materials & architecture docs
compose.yml     → Docker deployment configuration
.env            → Environment configuration

------------------------------------------------------------
INSTALLATION & SETUP
------------------------------------------------------------

1. Download all project files from GitHub and extract them.

2. Open the project folder:

Cybersecurity-Projects/PROJECTS/intermediate/siem-dashboard

3. Start Docker Desktop and wait until Docker Engine is running.

Download Docker Desktop:
https://www.docker.com/products/docker-desktop/

4. Open CMD/Terminal inside the siem-dashboard folder and run:

docker compose -f compose.yml up --build

This will automatically start:
- MongoDB
- Redis
- Backend API
- Frontend Dashboard
- Nginx Reverse Proxy

------------------------------------------------------------
ACCESS THE DASHBOARD
------------------------------------------------------------

Open in browser:

http://localhost:8431

------------------------------------------------------------
FIRST TIME USAGE
------------------------------------------------------------

1. Register a new account
2. Create username and password
3. Login to access dashboard features

After login you can explore:
- Alerts
- Dashboard
- Logs
- Correlation Rules
- Attack Scenarios

------------------------------------------------------------
IMPORTANT NOTE
------------------------------------------------------------

The dashboard will initially appear mostly empty because no security logs/events exist yet.

This is expected behavior.

The SIEM becomes interactive after:
- ingesting logs
- triggering attack simulations
- generating alerts
- creating detection rules

------------------------------------------------------------
SIEM WORKFLOW
------------------------------------------------------------

Attack Simulation / Logs
            ↓
      Correlation Engine
            ↓
        Alert Creation
            ↓
     Dashboard Visualization

------------------------------------------------------------
LEARNING MODULES
------------------------------------------------------------

The project includes detailed learning resources inside the learn/ folder.

00 - Overview       → Setup & prerequisites
01 - Concepts       → SIEM & SOC fundamentals
02 - Architecture   → Data flow & system design
03 - Implementation → Backend & frontend walkthrough
04 - Challenges     → Exercises & extension ideas

------------------------------------------------------------
USEFUL DOCKER COMMANDS
------------------------------------------------------------

Stop Containers:
docker compose down

Restart Project:
docker compose -f compose.yml up

Rebuild Containers:
docker compose -f compose.yml up --build

View Logs:
docker compose logs -f

------------------------------------------------------------
EDUCATIONAL PURPOSE
------------------------------------------------------------

This project is designed for:
- Cybersecurity students
- SOC analyst practice
- SIEM architecture learning
- Detection engineering basics
- Security monitoring demonstrations
- Portfolio projects

It is not intended for production security monitoring.
