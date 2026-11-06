CUET eFootball Championship — React + Firebase (no Vite)

FILES
- index.html: app entry point
- app.jsx: React application + Firebase connection + roster data
- styles.css: visual styling
- firestore.rules: recommended Firestore security rules

IMPORTANT PRIVACY NOTE
The supplied phone numbers and student IDs are intentionally not included in the app. The public tournament portal only needs owner name, eFootball username, division, group, fixtures and scores.

FIREBASE SETUP
1. Go to https://console.firebase.google.com/ and create a Firebase project.
2. Add a Web App and copy its Firebase config.
3. In app.jsx, replace the firebaseConfig placeholder values.
4. Replace ADMIN_EMAIL with your admin email.
5. In Firebase Console > Authentication > Sign-in method, enable Email/Password.
6. In Authentication > Users, add your admin email and password.
7. In Firestore Database, create a database (production mode is fine).
8. Publish firestore.rules after replacing YOUR_ADMIN_EMAIL@example.com with the same admin email.
9. Host the folder on a static host that serves ES modules over HTTPS (Netlify works). Do not open index.html directly as a file; use a local static server or hosting.

NO VITE / NO BUILD STEP
This app loads React, Babel and Firebase from CDNs. Babel compiles JSX in the browser. It does not require npm, Vite, or a bundler.

HOW TO USE
- Public tabs: Overview, Groups, Fixtures & Results, Knockout.
- Admin: click Admin login, sign in with the Firebase admin account.
- Assign teams to groups in Admin. There are 48 slots: the first 36 are prefilled, and the remaining 12 are TBD.
- Add fixtures and enter scores. Group standings update from completed group fixtures.
- Add knockout matches manually after deciding the qualification/bracket rules.

IMPORTANT
The initial group assignments are blank by design. Add groups after the final draw. This app does not assume the tournament's unresolved 12-team bye/knockout structure.
