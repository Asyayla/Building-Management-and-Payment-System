# Building Management & Payment System

A full-stack web application for managing residential buildings. Track apartments, their occupancy and the payments recorded for each one from a single dashboard.

---

## Overview

The backend exposes a RESTful API built with ASP.NET Core (.NET 8) and Entity Framework Core. The frontend is a React 19 single-page application written in TypeScript. Data is stored in a SQLite database that the API creates automatically on first run, so the project runs without any external infrastructure.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | .NET 8 (ASP.NET Core Web API), Entity Framework Core |
| Frontend | React 19 + TypeScript |
| Styling | Tailwind CSS |
| Database | SQLite |
| Containerization | Docker + Docker Compose |

---

## Features

- Create, update and delete apartments (block, floor, unit number)
- Track occupancy status per apartment
- Record payments per apartment with amount, paid/unpaid status and date
- Full CRUD through a RESTful API
- Single-page frontend that works with the API

---

## Project Structure

```
Building-Management-and-Payment-System/
├── building-management-backend/      # .NET 8 Web API
│   ├── Controllers/
│   ├── Migrations/
│   ├── Models/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   └── Program.cs
├── building-management-frontend/     # React + TypeScript + Tailwind
│   ├── public/
│   ├── src/
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
git clone https://github.com/Asyayla/Building-Management-and-Payment-System.git
cd Building-Management-and-Payment-System

# 2. Start the backend
cd building-management-backend
dotnet restore
dotnet run --urls http://localhost:5287
# API runs at http://localhost:5287

# 3. Start the frontend (new terminal, from the repository root)
cd building-management-frontend
npm install
npm start
# Open the URL printed in the terminal
```

The frontend expects the API at `http://127.0.0.1:5287/api`. This is set in `building-management-frontend/.env`.

### Run the Backend with Docker

```bash
cd building-management-backend
docker-compose up --build
```

---

## Detailed Documentation

- Backend: [`building-management-backend/README.md`](building-management-backend/README.md)
- Frontend: [`building-management-frontend/README.md`](building-management-frontend/README.md)
