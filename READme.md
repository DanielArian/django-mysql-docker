# Django and MySQL on Docker

## Installation for dev

1. Copy `.env.dev.exemple` to `.env.dev` and edit values.

```bash
DEBUG=1
SECRET_KEY=generate-key-here    # CHANGE THIS
DJANGO_ALLOWED_HOSTS=localhost 127.0.0.1 0.0.0.0 [::1]      
DATABASE=mysql
SQL_ENGINE=django.db.backends.mysql
SQL_PORT=3306
SQL_DATABASE=mydb               # name of the database
SQL_ROOT_PASSWORD=rootpassword  # CHANGE THIS
SQL_USER=myuser                 # do not use 'root'
SQL_PASSWORD=myuserpassword     # CHANGE THIS
SQL_HOST=db
```

2. Run `docker compose --env-file .env.dev up --build`

3. Visit `http://localhost:8000`