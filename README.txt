TREE BOT — /survival THEN AFK

Behavior:
1. Waits until the bot has spawned and authentication is confirmed.
2. Waits the configured 4 seconds, then sends /survival.
3. If the server clearly reports an error/rejection, retries /survival after 5 seconds.
4. If the server confirms survival mode, it enters AFK/idle immediately.
5. If the server sends no clear error within 5 seconds, it assumes the command was accepted and stays AFK/idle.
6. It does not run farming/world actions in this idle configuration.

Run:
  npm install mineflayer mineflayer-pathfinder vec3
  node tree_bot_survival_retry.js

On PowerShell, if npm.ps1 is blocked, use:
  npm.cmd install mineflayer mineflayer-pathfinder vec3

Tests performed:
- JavaScript syntax check: PASS
- Built-in self-test: PASS x3
- No live Minecraft server connection was made during tests.

Notes:
- Command responses vary by server. A quiet 5-second window is treated as success.
- Keep the file private because it contains the account configuration from the original file.
