# Flask Skeleton

Windows-oriented Flask starter application.

## Quick Start

### Basics

1. Create and activate a virtualenv
2. Install the requirements

```powershell
git clone <this_repo>
cd <this_repo>

virtualenv env

.\env\scripts\activate.ps1
```

### Set Environment Variables

Update *project/server/config.py*, and then run:

```powershell
set-variable -name "APP_SETTINGS" -value "project.server.config.DevelopmentConfig"
```

or

```powershell
set-variable -name "APP_SETTINGS" -value "project.server.config.ProductionConfig"
```

### Create DB

```powershell
python manage.py create_db
python manage.py db init
python manage.py db migrate
python manage.py create_admin
python manage.py create_data
```

### Run the Application

With debug mode:

```powershell
set-variable -name "FLASK_DEBUG" -value True; python manage.py run
```

Without debug mode:

```powershell
set-variable -name "FLASK_DEBUG" -value False; python manage.py run
```

Access the application at the address [http://localhost:5000/](http://localhost:5000/).

### Testing

Without coverage:

```powershell
$ python manage.py test
```

With coverage:

```powershell
$ python manage.py cov
```
