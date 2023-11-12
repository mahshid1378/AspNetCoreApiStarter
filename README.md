AspNetCoreApiStarter
An ASP.NET Core (v2.1) Web API project to quickly bootstrap new projects. Includes Identity, JWT authentication w/ refresh tokens.

Setup
Uses Sql Server Express LocalDB (If using Visual Studio install it under Individual Components in the Visual Studio installer or install separately using this link.
Apply database migrations to create the db. From a command line within the Web.Api.Infrastructure project folder use the dotnet CLI to run :
Web.Api.Infrastructure>dotnet ef database update --context AppDbContext
Web.Api.Infrastructure>dotnet ef database update --context AppIdentityDbContext
Visual Studio
Open the solution file AspNetCoreApiStarter.sln and build/run.

Visual Studio Code
Open the src folder and F5 to build/run.

Swagger Enabled
To explore and test the available APIs simply run the project and use the Swagger UI.

The available APIs include:

POST /api/accounts - Creates a new user.
POST /api/auth/login - Authenticates a user.
POST /api/auth/refreshtoken - Refreshes expired access tokens.
GET /api/protected - Protected controller for testing role-based authorization.
