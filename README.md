# Registrar

A mobile-friendly student, teacher and payment manager built as an installable web app (PWA). It is designed for a single administrator and syncs records between devices using Firebase.

## Features in this first version

- Dashboard with student, teacher, collection and overdue counts
- Student records: name, phone, country, course, fee, assigned teacher, registration date and next payment date
- Teacher records with Ustaz, Ustaza or Teacher roles
- Payment records with amount, date, method, next due date and note
- In-app due-date reminders and basic income reports
- Search, responsive layout and installable app shell

## Publish it free with GitHub Pages

1. Open this repository's **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Choose branch **main** and folder **/(root)**, then tap **Save**.
4. Wait a few minutes. GitHub will show the public Pages address on that same screen.

## Connect Firebase (required for login and cloud sync)

1. Open https://console.firebase.google.com/ and create a Firebase project.
2. In **Authentication → Sign-in method**, enable **Email/Password**.
3. In **Firestore Database**, create a database.
4. In **Project settings → General → Your apps**, create a **Web app** and copy its Firebase configuration.
5. In this repository, open `index.html`, find `const firebaseConfig =`, and replace the six `PASTE_...` placeholder values with the matching values from Firebase.
6. Commit the change. Refresh the GitHub Pages app after it redeploys.
7. In Firebase **Firestore → Rules**, publish the rules from `firestore.rules`.
8. Open the published app, create your administrator login, and use the same login on your other devices.

## Important privacy and usage notes

- The Firestore rules restrict each signed-in account to its own records. Do not share your login.
- Firebase's web config is intended to be included in a web app; never put service-account credentials or private keys in this repository.
- The repository code and GitHub Pages site are public. Do not add real student records or private information to GitHub files.
- This version shows reminders inside the app when opened. It does not send background push notifications, SMS or email.
- The balance figure is a simple estimate (sum of course fees minus recorded payments), not a complete accounting ledger.
- This is an initial version: records can be added and deleted; editing existing records and more advanced reports are not yet included.
- GitHub Pages and Firebase have free quotas and terms. Staying within their free limits is necessary to keep hosting and data services free.
