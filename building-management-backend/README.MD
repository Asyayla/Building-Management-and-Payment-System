# Backend — Building Management & Payment System

ASP.NET Core Web API serving the building management and dues tracking system.

---

## Tech Stack

- **.NET 8.0** — ASP.NET Core Web API
- **SQLite 3.43.2** — Embedded relational database
- **Entity Framework Core** — ORM and migrations

---

## Project Structure

```
building-management-backend/
├── Controllers/                          # API route handlers
├── Migrations/                           # EF Core database migrations
├── Models/                               # Entity models
├── Properties/                           # Launch settings
├── data/                                 # SQLite database files
├── BuildingManagement.csproj             # Project file
├── BuildingManagement.db                 # SQLite database
├── BuildingManagement.sln                # Solution file
├── Dockerfile                            # Container image definition
├── docker-compose.yml                    # Multi-container setup
├── Program.cs                            # App entry point & middleware config
├── appsettings.json                      # Production configuration
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
# From the root of the repository
dotnet restore
dotnet run
```

The API will be available at `http://localhost:5000`.  
Swagger UI (if enabled) will be at `http://localhost:5000/swagger`.

### Database

SQLite database file (`BuildingManagement.db`) is created automatically on first run via EF Core migrations. No manual setup is required.

To apply migrations manually:

```bash
dotnet ef database update
```

### Docker

The project includes a `Dockerfile` and `docker-compose.yml` for containerised deployment:

```bash
docker-compose up --build
```

---

## Configuration

Environment-specific settings live in `appsettings.json`:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Data Source=building.db"
  }
}
```
