CSC Suite Firebase Spark - FINAL FIX V2

1) Open firebase-config.js.
2) In Firebase Console:
   Project Settings -> Your apps -> Web app -> SDK setup and configuration.
3) Copy the exact Web App config values.
4) Put the exact apiKey into:
   apiKey: "..."
5) Put the exact Realtime Database URL into:
   databaseURL: "..."
6) Do NOT use file:/// URLs.
7) Start the local server from this folder:
   npx -y http-server . -p 5500
8) Open:
   http://localhost:5500/admin.html

If Firebase still says API_KEY_INVALID:
- Google Cloud Console -> APIs & Services -> Credentials
- Check that the API key belongs to project cricket-c3052.
- For testing, set Application restrictions to None.
- Ensure Identity Toolkit API is enabled.
