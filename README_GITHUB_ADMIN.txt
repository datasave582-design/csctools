CSC SUITE — ADMIN GITHUB PACKAGE

Upload ALL files in this folder to the ROOT of a GitHub repository.

Then:
GitHub -> Settings -> Pages -> Deploy from a branch -> main -> /(root) -> Save

Admin URL:
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/admin.html

Firebase:
1. Authentication -> Settings -> Authorized domains
2. Add YOUR-USERNAME.github.io
3. firebase-config.js must contain the exact Web App config.
4. Realtime Database Rules must match database.rules.json.

Security:
- Keep customer files out of this repository if you do not want them publicly accessible.
- Admin access is protected by Firebase Authentication + admins/<ADMIN_UID> = true.
