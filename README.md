# Puerto Rico Trip Planner
Open `index.html`. To share edits between people, paste your Firebase web config
into the `FIREBASE_CONFIG` block near the top of `index.html`.
Firestore rules (Firebase console > Firestore > Rules):

    rules_version = '2';
    service cloud.firestore {
      match /databases/{database}/documents {
        match /{c}/{id} {
          allow read, write: if c in ['items', 'people', 'meta'];
        }
      }
    }
