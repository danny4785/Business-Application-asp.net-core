# ASP.NET Core Business Application Framework

A lightweight ASP.NET Core framework for building business applications with minimal complexity.

## Quick Start

1. **Clone and run:**
   ```bash
   git clone <repository>
   cd Business-Application-asp.net-core
   dotnet run -p osafw-app
   ```

2. **Configure database:**
   - Open `https://localhost:PORT/Dev/Configure`
   - Create database and click "Initialize DB"

3. **Start building:**
   - Controllers: `/osafw-app/App_Code/controllers/`
   - Models: `/osafw-app/App_Code/models/`
   - Templates: `/osafw-app/App_Data/template/`

## Key Features

- **MVC-like structure** - Controllers, Models, Templates
- **RESTful routing** - Automatic URL mapping
- **SQL Server integration** - Built-in database helpers
- **Bootstrap UI** - Modern responsive interface
- **Template engine** - ParsePage for views
- **Authentication** - Simple access levels
- **File uploads** - With optional S3 support

## Project Structure

```
/osafw-app/
  /App_Code/
    /controllers/     # Your controllers
    /models/          # Your models  
    /fw/              # Framework core
  /App_Data/
    /template/        # HTML templates
    /sql/             # Database scripts
  /wwwroot/           # Public web assets
  appsettings.json    # Configuration
```

## REST Mapping

Controllers automatically map to URLs:

- `GET /Controller` → `IndexAction()` (list)
- `GET /Controller/ID` → `ShowAction()` (view)
- `GET /Controller/new` → `ShowFormAction()` (new form)
- `GET /Controller/ID/edit` → `ShowFormAction()` (edit form)
- `POST /Controller` → `SaveAction()` (create)
- `POST /Controller/ID` → `SaveAction()` (update)
- `DELETE /Controller/ID` → `DeleteAction()` (delete)

## Configuration

Main settings in `appsettings.json`:

```json
{
  "appSettings": {
    "SITE_NAME": "Your App Name",
    "db": {
      "main": {
        "connection_string": "your-connection-string",
        "type": "SQL"
      }
    }
  }
}
```

## Documentation

- [ParsePage Templates](osafw-app/docs/parsepage.md)
- [Database Helpers](osafw-app/docs/db.md)
- [Dynamic Controllers](osafw-app/docs/dynamic.md)
- [Dashboard](osafw-app/docs/dashboard.md)

## Demo

See it in action: http://demo.engineeredit.com/

## License

See LICENSE file for details.