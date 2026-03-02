# 🏫 Smart Campus Network — Access Control System

A full-stack, real-time Smart Campus Access Control & Monitoring System built with **Next.js 16**, **Prisma**, **SQLite**, **Tailwind CSS**, and **shadcn/ui**.

---

## 🚀 Features

| Tab | Description |
|---|---|
| **Dashboard** | Live stats cards, hourly access flow chart, user distribution pie chart, recent activity & active alerts |
| **Users** | Manage campus users (Students, Staff, Faculty, Visitors), filter/search, export to CSV |
| **Gates** | Add/update campus gates, change status (Online / Offline / Maintenance / Locked) |
| **Access Control** | Simulate RFID / Biometric / Manual scans and view real-time results |
| **Alerts** | View and resolve security alerts with severity levels (Low → Critical) |
| **Analytics** | Weekly trends, anomaly detection, occupancy tracking, peak-hours heatmap |
| **IoT Monitor** | Live IoT device connectivity panel — sensor readings, signal strength & remote actions |
| **Map** | Interactive campus map with gate pins, gate schedule & visitor pass generator |
| **Reports** | Export access logs to CSV and print reports |

### Additional
- 🔐 **Admin authentication** — JWT-based login/logout
- 🌙 **Dark / Light mode** toggle
- 💬 **AI Chatbot** assistant for campus queries
- 📱 **Mobile-responsive** with bottom navigation bar
- 🔄 **Auto-refresh** (dashboard every 30 s, IoT every 10 s)

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Framework | Next.js 16 (App Router) |
| Language | TypeScript |
| Styling | Tailwind CSS v4 + shadcn/ui |
| Database | SQLite via Prisma ORM |
| Charts | Recharts |
| Icons | Lucide React |
| Animations | Framer Motion |
| Notifications | Sonner (toast) |
| Runtime | Node.js / Bun |

---

## 📁 Project Structure

```
src/
├── app/
│   ├── page.tsx          # Main dashboard (all tabs)
│   ├── layout.tsx        # Root layout
│   ├── globals.css       # Global styles
│   ├── login/            # Login page
│   └── api/              # API routes
│       └── access-control/
│           ├── dashboard/stats
│           ├── users/
│           ├── gates/
│           ├── access-logs/
│           ├── security-alerts/
│           ├── scan/
│           └── seed/
├── components/
│   ├── IoTMonitor.tsx    # IoT device connectivity & monitoring
│   ├── CampusMap.tsx     # Interactive campus map
│   ├── Chatbot.tsx       # AI assistant chatbot
│   ├── AnomalyDetector.tsx
│   ├── OccupancyTracker.tsx
│   ├── WeeklyTrends.tsx
│   ├── PeakHoursHeatmap.tsx
│   ├── GateSchedule.tsx
│   ├── VisitorPass.tsx
│   ├── MobileNav.tsx
│   └── ui/               # shadcn/ui components
├── lib/
│   ├── auth.ts           # Auth utilities
│   ├── db.ts             # Prisma client
│   └── export.ts         # CSV / print utilities
prisma/
├── schema.prisma         # Database schema
└── dev.db                # SQLite database
```

---

## ⚙️ Database Schema

| Model | Purpose |
|---|---|
| `Gate` | Campus entry/exit points |
| `CampusUser` | Students, Staff, Faculty, Visitors |
| `AccessLog` | Every gate scan record |
| `Authorization` | User-gate access rules (time-based) |
| `SecurityAlert` | System-generated alerts |
| `AdminUser` | Dashboard admin accounts |

---

## 🏃 Getting Started

### Prerequisites
- **Node.js** 18+ or **Bun** 1.x
- **npm** or **bun**

### 1. Install dependencies
```bash
npm install
# or
bun install
```

### 2. Configure environment
Create a `.env` file in the project root:
```env
DATABASE_URL="file:./prisma/dev.db"
JWT_SECRET="your-secret-key"
```

### 3. Set up the database
```bash
npm run db:push
# or
npm run db:generate
```

### 4. Start the development server
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

> The app will auto-seed sample data on first load.

---

## 📦 Available Scripts

| Script | Description |
|---|---|
| `npm run dev` | Start development server on port 3000 |
| `npm run build` | Build for production |
| `npm run start` | Start production server |
| `npm run lint` | Run ESLint |
| `npm run db:push` | Push Prisma schema to database |
| `npm run db:generate` | Generate Prisma client |
| `npm run db:migrate` | Run database migrations |
| `npm run db:reset` | Reset the database |

---

## 🔑 Default Login

After starting the server, use the seeded admin credentials to log in:

| Field | Value |
|---|---|
| Email | `admin@campus.edu` |
| Password | `admin123` |

---

## 📡 IoT Monitoring

The **IoT** tab provides a live device monitoring dashboard:
- **8 campus IoT nodes** — Controllers, Sensors, RFID Readers, Cameras, Gateways
- **Live sensor readings** — Temperature, Humidity, CO₂, Power consumption
- **Remote actions** — Restart, Power On/Off, Run Diagnostics
- **Auto-refresh** every 10 seconds

---

## 👥 Team

Smart Campus Network — Team Project  
*IoT & RFID/Biometric Integration | Real-time Monitoring*
