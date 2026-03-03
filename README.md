# Building Management & Payment System

Full-stack building management and payment system.

---

## Key Features

- Manage apartments: add, update, delete, track occupancy
- Track payments: amount, paid/unpaid, creation date
- RESTful API with full CRUD operations
- Frontend built with React

---

## Tech Stack

- **Backend:** .NET 8.0  
- **Frontend:** React 19.1.1  
- **Database:** SQLite 3.43.2  

---

## Concepts Demonstrated

- Full-stack development (Frontend + Backend)  
- Database design and management (SQLite)  
- RESTful API design and implementation  
- Integration of frontend and backend

---

## Run Locally

```bash
# Clone repo
git clone https://github.com/Asyayla/building-management-and-payments.git
cd building-management-and-payments

# Backend
dotnet restore
dotnet run

# Frontend (in a new terminal)
cd frontend
npm install
npm start
