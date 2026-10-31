# Changelog

All notable changes to SoftNix Server are listed here.

## [1.0.0] — 2026-10-31

First public release. 🎉

### Web server
- Apache (mod_php) and Nginx (PHP FastCGI pool) — switch from the menu
- PHP 8.2, 8.3, 8.4 and 8.5 — one-click install and switch
- Automatic `*.test` domains for every folder in `www`, with HTTPS from a local certificate authority

### Databases
- MariaDB / MySQL (multiple versions), default login `root` / `root`, optional strong random password
- phpMyAdmin and Adminer (local only), SQLite + `sqlite3` command line
- One-click project database with its own user; `.sql` import; import databases from Laragon

### Laravel & PHP
- Quick app: Laravel, WordPress, blank PHP
- Composer and Node.js 24 LTS; terminal with the right PATH
- Procfile tasks (Vite, scheduler, any command) started with *Start all*

### Realtime mode
- Redis (password protected), Laravel Reverb WebSocket, queue worker
- WiFi / LAN share with QR code; firewall rule limited to private networks

### Mail
- Mailpit inbox; switch project mail between Mailpit and real SMTP

### App
- Light / dark theme, system tray, start with Windows, logs viewer, settings
- First-time setup that downloads the selected servers (SHA-256 verified)
- Built-in updates from GitHub Releases
- Installer with update detection; uninstall keeps projects and databases
