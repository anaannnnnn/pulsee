# Pulse — personal streaming app (mobile web / PWA)

Requires Node 20+.

## Run on your computer
1. cd server && cp .env.example .env   (fill in PCLOUD_CLIENT_ID, PCLOUD_CLIENT_SECRET, TPDB_API_KEY, TORBOX_API_KEY)
2. npm install
3. cd ../web && npm install && npm run build
4. cd ../server && npm start        -> open http://localhost:8787 (the server also serves the built web app)
   On your phone (same Wi-Fi) open http://<your-computer-LAN-IP>:8787 and use "Add to Home Screen".
   Turn on the passcode in Settings > Privacy so others on your network can't open it.

## Connect pCloud
In your pCloud app settings register the redirect URI: http://localhost:8787/api/pcloud/callback
(works when you authorize from the computer running the server). Or use the paste-a-code option on the pCloud page in the app.

## Demo mode (no keys needed)
cd server && npm run demo, or add ?mock=1 to the web URL.

API contract for the future iOS app: docs/API.md
