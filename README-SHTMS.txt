SHTMS COMPLETE STARTER PACKAGE

CENTRAL MODEL
Admin creates master data once. Other portals consume the same Firestore data.

BUILD ORDER
1. Faculty
2. Department -> Faculty
3. Programme -> Department
4. Course -> Department + Programme + Level
5. Students -> Faculty + Department + Programme + Level
6. Lecturers -> Faculty + Department + Programme + assigned Courses/Levels
7. Course Registration -> Student + Course
8. Lecturer Notes -> Lecturer + Course
9. Assignments -> Lecturer + Course + registered students
10. Attendance -> Lecturer + Course + registered students
11. Results/Examinations/Fees/etc.
12. Re-enable strict Firebase authentication and role/page authorization after the data model is stable.

IMPORTANT
The included placeholder modules are intentionally simple. They prevent a missing module from being confused with an Admin access error while the real module is built.
