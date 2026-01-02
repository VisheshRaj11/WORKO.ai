# WORKO.ai
A smart workflow automation platform that analyzes professional work patterns, visualizes productivity insights, and automates repetitive tasks using MERN, n8n, Redis, and Docker.

This project is a smart automation platform that helps professionals understand how they work and automatically handles boring, repetitive tasks.

It collects work data from tools such as GitHub, Notion, Zapier, System Tasks, and Calendar, sends this data to an n8n automation agent, and then:

Analyzes the user’s work patterns

Generates structured JSON insights

Displays productivity data on the frontend using graphs and charts

Automatically performs repetitive tasks like:

Scheduling meetings

Updating Notion documents

Triggering Zapier workflows

Why this project?

Most professionals:

Feel busy but don’t know where their time is going

Waste time on repetitive manual work

Forget follow-ups and scheduling

Don’t know their most productive time of day

Existing tools are often too complex or require heavy manual setup.
This platform solves that by automating workflow analysis and actions intelligently, while clearly explaining the insights.

🧠 How It Works (High-Level Flow)

Data Collection
Data is collected from:

GitHub (coding activity)

Calendar (meetings)

System Tasks (task progress)

Notion (notes and plans)

Zapier (automation triggers)

n8n Agent (Automation Brain)
The n8n agent:

Cleans and normalizes incoming data

Analyzes work patterns over time

Identifies productivity insights

Decides which tasks should be automated

JSON Insights
n8n sends structured JSON to the backend containing:

Best working time

Meeting impact on productivity

Task completion efficiency

Time-wasting activities

Backend & Frontend

Backend stores and caches insights

Frontend visualizes data using graphs and logs

Automated Actions
Based on analysis, the system automatically:

Schedules meetings

Updates Notion summaries

Triggers Zapier workflows

Handles reminders and repetitive tasks

All actions happen without manual effort.

🏗️ System Architecture
GitHub / Calendar / Tasks / Notion / Zapier
                    ↓
                n8n Agent
        (Analysis + Automation Decisions)
                    ↓
           JSON Insights & Actions
                    ↓
Backend (Node.js + Express)
        ↓              ↓
   MongoDB          Redis
        ↓
Frontend (React + Graphs)

🧰 Tech Stack
Frontend

React

Tailwind CSS

Chart libraries for data visualization

Backend

Node.js

Express.js

MongoDB

Automation

n8n (workflow automation agent)

Zapier (cross-tool automation)

Infrastructure

Redis (caching)

Docker (containerization)

▶️ Commands to Run
Prerequisites

Node.js (v18 or later recommended)

Docker & Docker Compose

MongoDB (or Dockerized MongoDB)

Redis (or Dockerized Redis)

1️⃣ Clone the Repository
git clone https://github.com/VisheshRaj11/WORKO.ai.git
cd your-repo-name

2️⃣ Start Infrastructure (MongoDB, Redis, n8n)
docker-compose up -d

3️⃣ Run Backend
cd backend
npm install
npm run dev

4️⃣ Run Frontend
cd frontend
npm install
npm run dev

5️⃣ Access Services

Frontend: http://localhost:5173

Backend API: http://localhost:5000

n8n Dashboard: http://localhost:5678
