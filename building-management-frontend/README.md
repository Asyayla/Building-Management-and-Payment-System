# Building Management & Payment System - Frontend

React single-page application for managing apartments and tracking payments. Built with TypeScript and styled with Tailwind CSS.

---

## Tech Stack

- **React 19**
- **TypeScript**
- **Tailwind CSS**
- **Create React App**
- Talks to the .NET backend over HTTP

---

## Project Structure

```
building-management-frontend/
├── public/                   # Static assets & index.html
├── src/                      # Application source code
├── .env                      # API base URL
├── tailwind.config.js        # Tailwind CSS configuration
├── tsconfig.json             # TypeScript compiler configuration
├── package.json
└── README.md
```

---

## Getting Started

### Prerequisites

- [Node.js 18+](https://nodejs.org/) and npm
- The backend running at `http://127.0.0.1:5287` (see the backend README)

### Install & Run

```bash
cd building-management-frontend
npm install
npm start
```

Open the URL printed in the terminal.

---

## Available Scripts

| Script | Description |
|---|---|
| `npm start` | Start the development server with hot reload |
| `npm test` | Run tests in interactive watch mode |
| `npm run build` | Build the production bundle to `/build` |

### Production Build

```bash
npm run build
```

The output goes to the `build/` folder as static files that any web server can serve.

---

## Connecting to the Backend

The API base URL is read from `.env`:

```
REACT_APP_API_URL=http://127.0.0.1:5287/api
```

Update it to match your backend host when deploying. Restart `npm start` after changing it.
