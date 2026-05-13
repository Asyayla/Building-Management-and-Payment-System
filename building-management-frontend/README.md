# Frontend — Building Management & Payment System

React single-page application for managing apartments and tracking monthly dues. Built with TypeScript and styled with Tailwind CSS.

---

## Tech Stack

- **React 19.1.1**
- **TypeScript**
- **Tailwind CSS**
- **Create React App**
- Communicates with the .NET backend over HTTP

---

## Project Structure

```
building-management-frontend/
├── public/                   # Static assets & index.html
├── src/                      # Application source code
├── .env                      # Environment variables (API base URL etc.)
├── tailwind.config.js        # Tailwind CSS configuration
├── tsconfig.json             # TypeScript compiler configuration
├── package.json
└── README.md
```

---

## Getting Started

### Prerequisites

- [Node.js 18+](https://nodejs.org/) and npm

### Install & Run

```bash
cd building-management-frontend
npm install
npm start
```

The app will open at [http://localhost:3001](http://localhost:3001).  
It expects the backend to be running at `http://localhost:5000`.

---

## Available Scripts

| Script | Description |
|---|---|
| `npm start` | Start development server with hot reload |
| `npm test` | Run tests in interactive watch mode |
| `npm run build` | Build optimised production bundle to `/build` |

### Production Build

```bash
npm run build
```

Output goes to the `build/` folder — minified, hashed, and ready to serve as static files behind any web server (Nginx, Apache, etc.).

---

## Connecting to the Backend

API base URL is set in `src/services/` (or `.env` if configured). Update it to match your backend host when deploying:

```
REACT_APP_API_URL=http://localhost:5000
```
