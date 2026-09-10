SHTMS STEP — MANAGE LECTURERS

New lecturer-management.html:
- Lecturer master records in users/{UID}, role="lecturer"
- Staff ID, name, contact, photo, rank, discipline, status
- Faculty -> Department -> Programme cascading selection
- Assigned courses stored as assignedCourseIds
- Search and filters
- Edit/delete master record (does not delete Firebase Authentication account)

This uses the existing school structure collections:
faculties, departments, programmes, courses.

Next modules can use assignedCourseIds for timetable, lecture notes,
assignments, attendance and results.
