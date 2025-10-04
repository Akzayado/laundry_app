# laundry_app

## Laravel Docker Starter
A laravel project running with Docker, featuring:
- PHP 8.2 + Apache
- Composer
- Node.js (for Vite/Frontend)
- PostgreSQL (database)
- pgAdmin (database GUI)
  
## 🚀 Getting Started
### 1. Clone the repository
```
git clone https://github.com/yourusername/laravel-docker.git
cd laravel-docker
```

### 2. Copy environment file
```
cp .env.example .env
```
Update .env if needed (DB credentials, app URL, etc.).

### 3. Build and start containers
```
docker-compose up -d --build
```
### 4. Install PHP dependencies
```
docker exec -it laravel_app composer install
```
### 5. Generate Laravel app key
```
docker exec -it laravel_app php artisan key:generate
```
### 6. Run migrations
```
docker exec -it laravel_app php artisan migrate
```
### 7. Node.js frontend
```
npm run dev
```
For production build:
```
docker exec -it laravel_node npm run build
```
## 🐘 Services
| Service    | URL                                            | Notes                                  |
| ---------- | ---------------------------------------------- | -------------------------------------- |
| Laravel    | [http://localhost:8080](http://localhost:8080) | PHP 8.2 + Apache                       |
| PostgreSQL | localhost:5432                                 | DB: `laravel_db`                       |
| pgAdmin    | [http://localhost:5050](http://localhost:5050) | Email: `admin@admin.com` / PW: `admin` |

## 🛠 Useful Commands
- Enter Laravel container (app):
```
docker exec -it laravel_app bash
```
- Run Artisan::
```
docker exec -it laravel_app php artisan migrate
```
- Install Composer deps:
```
docker exec -it laravel_app composer install
```
- Install Node deps:
```
docker exec -it laravel_node npm install
```
