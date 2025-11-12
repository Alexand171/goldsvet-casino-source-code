# Goldsvet Open Source
**Last Update : 2025**

**This version comes with support for:**

- Laravel 10
- PHP 8.2+
- Node.js

**Also includes plugin support for:**

- Sports Betting
- Crypto Competitions
- Stock Competitions

**Note**: Plugins and games are available for subscribers in Discord downloads.
**Subscribe**: On our Discord, you will find updated files with games.

## Key Features

- **1320 games available (as of late sep 2025), including 100 from Pragmatic Play**
- **GeoIP2 support (manually enabled)**

## Getting Started

**Official Discord**: [Join Here](https://discord.gg/eX3smYUgSX)

## Setup Instructions

Here’s a guide for setting up the project on a typical cPanel server. It can be adapted for other environments.

1. **Server Setup Requirements**:
   - Apache, MySQL
   - PHP 8+ (Composer required)
   - Laravel 10
   - Node.js 16 & PM2
2. **Enable SSL**: Force SSL for your domain.
3. **Create Database**: Set up a MySQL database for the app.
4. **Clone the Repository**: Pull the latest code from GitHub.
5. **Install Dependencies**:
   ```bash
   composer install
   npm install
   ```
6. **Environment Configuration**:
   - Copy `.env.example` to `.env` and update with your environment variables.
   ```bash
   php artisan key:generate
   ```
7. **Migrate Database**:
   ```bash
   php artisan migrate
   ```

> **Tip**: Check out the full [PM2 Commands Guide](https://pm2.keymetrics.io/docs/usage/quick-start/) for managing Node.js processes.

## PM2 Commands for WebSockets

Inside the `PTWEBSOCKET` folder, use the following commands:

```bash
pm2 start Arcade.js --watch
pm2 start Server.js --watch
pm2 start Slots.js --watch
```

To start all services at once:

```bash
pm2 start Arcade.js --watch && pm2 start Server.js --watch && pm2 start Slots.js --watch
```

## Troubleshooting

If you run into issues, try clearing caches:

```bash
php artisan cache:clear
php artisan config:clear
php artisan route:clear
```

### Common Errors

- **404 Errors**: Ensure your `.htaccess` file is properly set up.
