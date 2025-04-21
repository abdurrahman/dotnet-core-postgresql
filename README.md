# dotnet-core-postgresql

A sample MVC project about how to use PostgreSQL with ASP.NET Core.

You can take a look [Medium post](https://medium.com/@isikabdurrahman/net-core-ile-postgresql-kullan%C4%B1m%C4%B1-7aa025ec9123) for detailed instructions [TR]

This project uses;
- .NET 9.0 target framework.
- Npgsql.EntityFrameworkCore.PostgreSQL 9.0.4 NuGet package.

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
