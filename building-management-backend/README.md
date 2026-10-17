# Building Management & Payment System - Backend

ASP.NET Core Web API for managing apartments and recording payments.

---

## Tech Stack

- **.NET 8.0** — ASP.NET Core Web API
- **SQLite** — embedded relational database
- **Entity Framework Core** — ORM and migrations

---

## Data Model

| Entity | Fields |
|---|---|
| `Apartment` | `Id`, `Block`, `Floor`, `Number`, `IsOccupied` |
| `Payment` | `Id`, `ApartmentId` (foreign key to `Apartment`), `Amount`, `Paid`, `CreatedAt` |

Each payment belongs to one apartment, so the payments of an apartment form its payment history.

---

## Project Structure

```
building-management-backend/
├── Controllers/                          # API route handlers
├── Migrations/                           # EF Core database migrations
├── Models/                               # Entities and DTOs
├── Properties/                           # Launch settings
├── data/                                 # SQLite database files
├── BuildingManagement.csproj             # Project file
├── BuildingManagement.sln                # Solution file
├── Dockerfile                            # Container image definition
├── docker-compose.yml                    # Docker Compose setup
├── Program.cs                            # App entry point & middleware config
├── appsettings.json                      # Configuration
└── appsettings.Development.json          # Development configuration
```

---

## API Endpoints

### Apartments

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/apartments` | List all apartments |
| GET | `/api/apartments/{id}` | Get apartment by ID |
| POST | `/api/apartments` | Create a new apartment |
| PUT | `/api/apartments/{id}` | Update an apartment |
| DELETE | `/api/apartments/{id}` | Delete an apartment |

### Payments

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/payments` | List all payments |
| GET | `/api/payments/{id}` | Get payment by ID |
| POST | `/api/payments` | Record a new payment |
| PUT | `/api/payments/{id}` | Update a payment |
| DELETE | `/api/payments/{id}` | Delete a payment |

---

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)

### Run

```bash
cd building-management-backend
dotnet restore
dotnet run --urls http://localhost:5287
```

The API will be available at `http://localhost:5287`. In the Development environment, Swagger UI is served at `http://localhost:5287/swagger`.

### Database

The SQLite database is created automatically on first run: the app applies the EF Core migrations at startup (`Database.Migrate()` in `Program.cs`). No manual setup is required, and the database file is not committed to the repository.

To apply migrations manually:

```bash
dotnet ef database update
```

### Docker

The project includes a `Dockerfile` and a `docker-compose.yml`:

```bash
docker-compose up --build
```

---

## Configuration

The database connection string is set in `appsettings.json` under `ConnectionStrings:DefaultConnection`. Environment-specific overrides go in `appsettings.Development.json`.
