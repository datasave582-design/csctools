# CSC Suite — Firebase Spark / GitHub Pages

A browser-based CSC document, photo and PDF utility suite with Firebase Authentication + Realtime Database licensing.

## GitHub Pages setup

1. Upload **all files in this folder** to the root of a GitHub repository.
2. In GitHub: **Settings → Pages → Deploy from a branch → main → /(root) → Save**.
3. Wait for the Pages deployment.
4. Open the site URL and use `/admin.html` for the admin panel.

## Firebase configuration

Before using Authentication/Database, edit `firebase-config.js` and paste the exact Web App configuration from:

**Firebase Console → Project settings → Your apps → Web app → SDK setup and configuration**

Set at minimum:

- `apiKey`
- `authDomain`
- `databaseURL`
- `projectId`
- `storageBucket`
- `messagingSenderId`
- `appId`

Do not invent the `databaseURL`.

## Firebase Authentication

Enable **Email/Password** under Authentication → Sign-in method.

Create the Admin user under Authentication → Users.

Then in Realtime Database create:

```text
admins/<ADMIN_FIREBASE_UID> = true
```

Use Boolean `true`, not the string `"true"`.

## Firebase Authorized Domain

After GitHub Pages is live, add the GitHub Pages hostname to:

**Firebase Console → Authentication → Settings → Authorized domains**

Example:

```text
YOUR-USERNAME.github.io
```

## Realtime Database rules

The supplied `database.rules.json` is the Spark-compatible rules file used by this package. Publish the rules in Firebase Console or deploy them with the Firebase CLI.

## Important

GitHub Pages hosts the frontend only. It does **not** provide a secure server/backend. Firebase Authentication and Realtime Database remain the backend services.

The current Spark license system is browser/client-side software protection; it is not equivalent to server-side DRM. For stronger enforcement, a trusted backend/Cloud Functions architecture is required.

Developer contact: +91 93238 838
