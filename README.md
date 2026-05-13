# Building Management & Payment System

A full-stack web application for managing residential buildings — track apartments, residents, and monthly dues from a single dashboard.

---

## Overview

This project provides building administrators with a clean interface to manage apartment units and monitor payment status. The backend exposes a RESTful API built with .NET 8, while the frontend is a React 19 single-page application. Data is persisted in a lightweight SQLite database, making the system easy to run without any external infrastructure.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | .NET 8.0 (ASP.NET Core Web API) |
| Frontend | React 19.1.1 + TypeScript |
| Styling | Tailwind CSS |
| Database | SQLite 3.43.2 |
| Containerisation | Docker + Docker Compose |

---

## Features

- Add, update, and delete apartment units
- Track occupancy status per unit
- Record and monitor monthly dues (paid / unpaid)
- Full CRUD operations via RESTful API
- Responsive single-page frontend

---

## Project Structure

```
Building-Management-and-Payment-System/
├── building-management-backend/      # .NET 8 Web API
│   ├── Controllers/
│   ├── Migrations/
│   ├── Models/
│   ├── data/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   └── Program.cs
├── building-management-frontend/     # React + TypeScript + Tailwind
│   ├── public/
│   ├── src/
│   ├── .env
│   ├── tailwind.config.js
│   └── tsconfig.json
└── README.md
```

---

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- [Node.js 18+](https://nodejs.org/) and npm

### Run Locally

```bash
# 1. Clone the repository
git clone https://github.com/Asyayla/building-management-and-payments.git
cd Building-Management-and-Payment-System

# 2. Start the backend
cd building-management-backend
dotnet restore
dotnet run
# API runs at http://localhost:5000

# 3. Start the frontend (new terminal)
cd building-management-frontend
npm install
npm start
# App runs at http://localhost:3001
```

---

## Detailed Documentation

- Backend: [`building-management-backend/README.md`](building-management-backend/README.md)
- Frontend: [`building-management-frontend/README.md`](building-management-frontend/README.md)└── README.md
```

---

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- [Node.js 18+](https://nodejs.org/) and npm

### Run Locally

```bash
# 1. Clone the repository
git clone https://github.com/Asyayla/building-management-and-payments.git
cd Building-Management-and-Payment-System

# 2. Start the backend
cd building-management-backend
dotnet restore
dotnet run
# API runs at http://localhost:5000

# 3. Start the frontend (new terminal)
cd building-management-frontend
npm install
npm start
# App runs at http://localhost:3001
```

---

## Detailed Documentation

- Backend: [`building-management-backend/README.md`](building-management-backend/README.md)
- Frontend: [`building-management-frontend/README.md`](building-management-frontend/README.md)
