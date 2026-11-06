## SoftNix Server 1.1.0

The biggest update so far: the tools you used to install separately are now inside SoftNix Server.
Optional tools are downloaded **only when you use them** (you are asked first) and can be removed in **Settings → Downloads**.

### ✨ New
- 🏠 **Dashboard at `http://localhost`** — all your projects (Laravel version, database), running services, phpMyAdmin, Adminer, Mailpit and phpinfo. Only visible on this PC, works offline.
- 🧩 **PHP → Extensions** — turn gd, intl, zip, sodium, pgsql… on or off with a tick
- ⚙️ **PHP → Quick settings** — upload size, memory limit, max execution time in one click
- 🐞 **Xdebug** on/off (PHP menu) for VS Code / PhpStorm
- 🟢 **Node.js versions** — download Node 20, 22 or 24 and switch (Tools → Node version)
- 🐘 **PostgreSQL** (Quick add) — runs on this PC only; "Use PostgreSQL database" fills the project `.env`
- 🔍 **Dumps & Logs** (new *Dumps* button) — `dump()` / `dd()` appear in a window instead of the page, plus `laravel.log` live with *Errors only*
- ⏰ **Scheduler on/off** per project — Laravel's scheduler runs every minute
- 💾 **Database snapshots** per project — save and restore in one click (MySQL / MariaDB, PostgreSQL, SQLite)
- 🌍 **Share online** — a temporary public https link for client demos and webhook tests
- 🚀 **Deploy to live** — upload only the changed files to your hosting over SSH, run migrations, maintenance page while updating

You find the project tools in **Menu → www → your project**.

### 🛠 Fixed
- Updating no longer takes minutes: the Microsoft runtime was downloaded and installed again on every update
- Setup no longer shows "Not responding" at the end (statistics are sent in the background)
- No more "unknown variable mysqlx" warnings in the MariaDB log and "Unclean shutdown" warnings in the Apache log

### Update
Open SoftNix Server → **Update now** (or Help → Check for updates). Projects, databases and settings are kept.
