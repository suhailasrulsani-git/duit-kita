# Duit Kita

A small family money app for the phone. Husband and wife share one live view of:

- Net salary for each person
- Monthly commitments (they repeat every month until removed)
- Spending, per person and per category
- One family budget per category
- Shared savings goals, with how long each goal will take
- Money to pay back (for example to parents), with a progress picture and message to share
- A savings forecast for 3, 6 and 12 months
- Events on a calendar, each with things to buy and prepare before a date

Money is in RM. Open the page on the phone and use "Add to Home Screen" to install it as an app.

## How it works

- One `index.html`, no build step. Hosted on GitHub Pages.
- Data lives in Firebase (Firestore) and syncs live between phones.
- Sign-in is with Google. The Firestore rules allow only the family's Google accounts.
- Until `firebase-config.js` is filled in, the app runs in demo mode and keeps data on that phone only.

## Setup

1. Create a Firebase project. Turn on Google sign-in and Firestore.
2. Add your GitHub Pages domain under Authentication > Settings > Authorized domains.
3. Put your Google accounts in the Firestore rules.
4. Paste the web app config into `firebase-config.js`.

The Firebase web config is not secret. The Firestore rules protect the data.
