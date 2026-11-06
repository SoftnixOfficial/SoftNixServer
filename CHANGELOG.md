# Changelog

All notable changes to SoftNix Server are listed here.

## [1.1.0] — 2026-11-07

### New
- Local dashboard at `http://localhost` (projects, services, tools; this PC only, offline)
- PHP → Extensions on/off, PHP → Quick settings (upload size, memory, execution time), Xdebug on/off
- Node.js 20 / 22 / 24 side by side (Tools → Node version)
- PostgreSQL add-on (Quick add) + "Use PostgreSQL database" for projects
- Dumps & Logs window (`dump()` / `dd()` via var-dump-server, `laravel.log` live)
- Per project: Scheduler on/off, Database snapshot (save / restore), Share online (Cloudflare quick tunnel), Deploy to live (SSH, changed files only)
- Settings → Downloads: list and remove optional add-ons; optional tools are downloaded only after asking

### Fixed
- In-app update took 2-3 minutes (Microsoft VC++ runtime re-installed on every update)
- Setup "Not responding" while sending install statistics
- MariaDB `mysqlx` warnings and Apache "Unclean shutdown" warnings on every start

## [1.0.3] — 2026-11-06

### New
- **Move from Laragon** (Menu → Tools, and offered on first start): copies your projects and databases into SoftNix and
  points Laravel `.env` / WordPress `wp-config.php` at SoftNix's MySQL. Laragon itself is never changed.
- **Port conflict help**: when a port is taken (Laragon or XAMPP still running, a Windows service…) SoftNix says who has
  it and switches to a free port in one click
- **Report a bug / Request a feature** form inside the app (Help menu), and a one-time welcome card
- **New update window** with release notes, version badges and progress
- Uninstaller asks (optionally) why you are leaving — helps us improve

### Changed
- Mailpit SMTP now uses port **2525** by default (1025 is often taken by Windows)
- Anonymous daily "still in use" signal so we can see how many people really use SoftNix (turn off with setup `/NOSTATS`)

## [1.0.2] — 2026-10-31

### Fixed
- Terminal: `ls`, `ll`, `clear`, `pwd`, `cat`, `touch`, `grep`, `which`… now work in CMD (Laragon / Cmder style).
  If Git for Windows is installed its Linux tools are used, otherwise built-in shortcuts.
- Terminal prompt now follows `cd` and shows the current folder

### New
- `art` shortcut for `php artisan` (e.g. `art migrate`) in CMD and PowerShell

## [1.0.1] — 2026-10-31

### New
- 🎨 **New SoftNix terminal** — colorful banner (project, PHP / web server / database / Node versions, tips)
  and a two-line colored prompt, in CMD and PowerShell
- **Windows Terminal** support: opens a themed "SoftNix Server" profile (logo icon, SoftNix colors) when installed;
  the classic console is used otherwise
- Settings → Terminal: use PowerShell instead of CMD, Windows Terminal on/off

### Improved
- Realtime mode: when a Laravel project needs Predis, SoftNix offers to install it for you

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
