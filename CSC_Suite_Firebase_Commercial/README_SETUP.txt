CSC SUITE — FIREBASE SPARK FINAL SETUP

1. Firebase Console -> Authentication -> Sign-in method -> enable Email/Password.
2. Authentication -> Users -> create your Admin user. Copy its UID.
3. Realtime Database -> create database (Locked mode).
4. Realtime Database -> Rules -> paste database.rules.json and Publish.
5. Realtime Database -> Data -> create: admins/<YOUR_ADMIN_UID> = true
6. Create each customer in Authentication -> Users -> Add user. Copy customer UID.
7. Open admin.html through a local HTTP server, NOT file://. Example: npx -y http-server . -p 5500
8. Open http://localhost:5500/admin.html. Login as Admin.
9. Enter customer UID + License ID + plan and Create / Update License.
10. Give customer email/password and License ID.
11. Customer opens CSC_Suite_FINAL_COMMERCIAL.html through the same local HTTP server.
12. First successful license activation binds the browser/device ID. A different browser/PC is rejected.

IMPORTANT API KEY NOTE:
The supplied Firebase Web API key is embedded in the files. If Firebase returns API_KEY_INVALID, the HTML cannot repair a disabled/restricted key. In Google Cloud Console -> APIs & Services -> Credentials, open the Web API key for project cricket-c3052. For testing, set Application restrictions to None, ensure Identity Toolkit API is enabled, and save.

This Spark version does not use Cloud Functions or Blaze. It is client-side licensing, so it is practical but not unbreakable DRM.

Developer: +91 93238 838
