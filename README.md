MYAI SETUP
1. Cloudflare D1: create database `myai-db`.
2. Put its ID into wrangler.jsonc.
3. Run: npx wrangler d1 execute myai-db --remote --file=schema.sql
4. Worker Settings > Variables and Secrets:
   ADMIN_EMAIL = your own login email
   SESSION_SECRET = a long random value (kept for future security extensions)
5. GitHub build settings:
   Build command: EMPTY
   Deploy command: npx wrangler deploy
   Never put `/` in Deploy command.
6. Deploy.
7. Register with ADMIN_EMAIL. That account is recognized server-side as admin.
8. Admin page is `/admin` through the same MyAI site; only the configured admin email can use its API.
Privacy note: this version stores user chat messages in D1 and allows the configured administrator to view them. Tell users clearly and comply with applicable privacy law before public use.
