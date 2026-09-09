# SHTMS Login Page

This package contains only `index.html`.

## How role redirection works

1. User logs in with Firebase Authentication email/password.
2. The system gets the user's Firebase UID.
3. It reads this Firestore document:

Collection: users
Document ID: USER'S FIREBASE AUTH UID

Example document:

{
  "role": "student"
}

Supported roles:

student   -> student.html
lecturer  -> lecturer.html
lecture   -> lecturer.html
hod       -> hod.html
registrar -> registrar.html
bursary   -> bursary.html
admissions -> admissions.html
admin     -> admin.html

## Firebase setup

Enable:
Firebase Authentication -> Email/Password

Create:
Firestore Database

For every authenticated user, create a document in:
users/{Firebase Authentication UID}

with the field:
role: "student"

The destination HTML files must exist in the same folder as index.html.
