# NLW 5

## Setup

Setup default project:
```bash
curl -s "https://laravel.build/example-app" | bash
```

Setup custom project:
```bash
curl -s "https://laravel.build/olw-5?with=mysql,redis" | bash
```

Initialize containers:
```bash
cd olw-5 && ./vendor/bin/sail up
```

Create alias ():
```bash
cd olw-5
alias sail='./vendor/bin/sail'
```

Initialize containers:
```bash
sail up # Default
sail up -d # Detach Mode
```

Run migrations:
```bash
sail art migrate # Default
sail art migrate:fresh # Drop tables and run migrations
```

If everything went fine, Laravel should be up at ```localhost```.

## Auth

Setup authentication:
```bash
sail composer require laravel/breeze --dev
```

```bash
sail php artisan breeze:install
```

```
One new database migration has been published. Would you like to run all pending database migrations? (yes/no) [yes]:
> yes
```
