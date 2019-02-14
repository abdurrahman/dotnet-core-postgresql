# dotnet-core-postgresql

A sample MVC project about how to use PostgreSQL with ASP.NET Core.

This project uses;
- .NET Core 2.2 target framework.
- Npgsql.EntityFrameworkCore.PostgreSQL 2.2.0 package.

## Project Setup

### Clone repo

```bash
$ git clone https://github.com/abdurrahman/dotnet-core-postgresql.git
``` 

### Update appsettings.json

Configure connection string in project's appsettings.json, replacing the `username`, `password`, and `dbname` appropriately (Consider to change Server name if it necessary):

```json
"ConnectionStrings": {
    "DefaultConnection": "User ID=username;Password=password;Server=localhost;Port=5432;Database=dbname;Integrated Security=true;Pooling=true;"
},
```

### Running the migration

Execute the following comment inside the project directory, **where the .csproj file is located**:

    $ dotnet ef database update

After running the migration, the database is created and web application is ready to be run.