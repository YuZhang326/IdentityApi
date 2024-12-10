# Identity API Demo

This is an ASP.NET Core Web API project that demonstrates the integration of ASP.NET Core Identity for user authentication and authorization. The project uses SQLite as the database provider and supports automatically generated Identity APIs.

---

## Project Structure


---

## Features

1. **ASP.NET Core Identity**:
   - Configures Identity for user authentication and authorization.
   - Supports `AppUser` as the custom user model inheriting from `IdentityUser`.

2. **SQLite Integration**:
   - Uses SQLite as the database provider for simplicity and easy setup.

3. **Automatically Generated Identity APIs**:
   - The `AddApiEndpoints()` method enables built-in Identity API endpoints for common user management actions like registration, login, and password reset.

4. **Authorization**:
   - Demonstrates securing APIs with the `[Authorize]` attribute.

5. **Swagger Integration**:
   - Includes Swagger for easy API exploration and testing.

---

## Prerequisites

- .NET 8.0 SDK or higher
- SQLite (installed locally or embedded)
- IDE or text editor like Visual Studio, VS Code, or JetBrains Rider

---

## Configuration

### appsettings.json
No specific configuration is required for this demo as SQLite is used with default settings. The connection string for SQLite is defined in `Program.cs`:

```csharp
opt.UseSqlite("DataSource=appdata.db");
```

# API Overview
# Identity Endpoints
The project includes automatically generated Identity endpoints, such as:
  POST /identity/register: Register a new user.
  POST /identity/login: Authenticate and get a bearer token.
  POST /identity/password-reset: Reset a user's password.
# Example Protected Endpoint
The WeatherForecastController demonstrates a protected API endpoint:
  GET /WeatherForecast:
  Requires an authorized user (Bearer token).
  Returns a list of random weather data.
