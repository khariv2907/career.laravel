# Career Laravel
- [Installation](#Installation)

## Installation
### Step 1. Build Docker containers
See [Building Docker containers guide](https://github.com/khariv2907/career.laradock)

### Step 2. Start Docker containers
Go to your laradock project root directory and then run:
```bash
make start
```

### Step 3. Copy .env file
In you project root directory run:
```bash
cp .env.example .env
```

### Step 4. Install dependencies
Go to your laradock project root directory and then run:
```bash
make bash
```
Install Composer dependencies
```bash
composer install
```

Install Node dependencies
```bash
npm ci
```

### Step 5. Generate key
```bash
php artisan key:generate
```

### Step 6. Permissions
Go to your project root directory and run:
```bash
sudo find . -type f -exec chmod 644 {} \;
sudo find . -type d -exec chmod 755 {} \;
sudo chmod -R 777 ./storage ./bootstrap/cache/ ./node_modules/
```
