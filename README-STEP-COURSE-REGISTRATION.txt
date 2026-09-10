SHTMS STEP — COURSE REGISTRATION / MANAGE STUDENT COURSES

This step adds course-registration.html to the central Admin workflow.

Features:
- Select a student from users where role == student.
- Select academic session, semester and level.
- Select one or more courses.
- Saves one courseRegistration document per student + course + session + semester.
- Stores stable studentId/courseId references plus display snapshots.
- Prevents duplicate registration records for the same student/course/session/semester.
- Search and filter existing registrations.
- Remove a registration.
- Admin Center now links to Course Registration.
- Firestore rules allow active admins to read/write courseRegistrations.

Important:
- Firebase Authentication accounts are not created by this page.
- Student master records remain in users/{studentUid}.
- Course master records remain in courses/{courseId}.
- Later lecturer functionality should query courseRegistrations by courseId and match lecturer assignedCourseIds.
- Because older student master records may currently contain programme/department names rather than IDs, the page supports name-based programme filtering when possible and keeps the stable IDs when available.
