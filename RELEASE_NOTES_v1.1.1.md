## SoftNix Server 1.1.1

A reliability release: a smoother first start, smarter port handling and automatic updates.

### 🛠 Fixed
- **First-time setup can no longer be interrupted by an update.** The app now checks for a new version first, then runs setup
- If a download failed or setup was closed half-way, **setup comes back** and **Retry only repeats what failed**. "Start all" no longer says "All services running" when the web server or PHP is missing
- **Clear download errors** — tells you when a site is blocked by your internet provider and what to try, instead of a technical message
- **MariaDB / MySQL**: a first start that was interrupted no longer blocks the database forever (the unfinished folder is moved aside, nothing is deleted)
- **Ports reserved by Hyper-V, WSL or Docker** are now detected, and SoftNix offers a free port
- **PostgreSQL** and the Nginx PHP workers switch to a free port automatically
- Clearer warning when MySQL moves to another port (projects must use the new `DB_PORT`)
- The installer refuses folders with spaces or non-English letters (they break Apache, MariaDB and Composer)

### 🔄 Changed
- **Updates are now required.** SoftNix checks GitHub every time it starts (and every 3 hours); a new version installs in a few seconds, so nobody stays on a version with known bugs. Without internet the app starts normally
- The update check also works when the GitHub API limit is reached on shared networks
- When you uninstall, you can include the last error lines of the SoftNix log (box is ticked, untick to skip) so we can see what went wrong

### Update
Open SoftNix Server → **Update now**. Projects, databases and settings are kept.
