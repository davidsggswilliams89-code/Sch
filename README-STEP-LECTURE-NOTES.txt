SHTMS STEP — LECTURE NOTES → COURSE → REGISTERED STUDENTS

Implemented:
1. Lecturer Portal (lecturer.html) now links to Lecture Notes and teaching tools.
2. lecture-notes.html lets an active lecturer choose one of their assigned courses.
3. Lecturer can upload PDF/DOC/DOCX/PPT/PPTX files up to 15 MB.
4. Each note is stored in Firestore collection: lectureNotes.
5. File is stored in Firebase Storage under lecture-notes/{lecturerUid}/.
6. Course registration now creates a courseAccess/{studentUid}__{courseId} marker.
7. Removing the registration removes that course-access marker.
8. Student Profile reads current course registrations and then loads lecture notes for those courses.
9. Firestore rules allow students to read notes only when they have a courseAccess marker for that course; lecturers can create notes only for assigned courses.
10. storage.rules is included for the lecture-notes Storage path.

IMPORTANT:
- Deploy firestore.rules and storage.rules in Firebase Console / Firebase CLI.
- Firebase Storage must be enabled in the project before file uploads can work.
- This step uses courseAccess markers so a student who becomes registered later can access notes already published for that course.
