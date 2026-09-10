SHTMS FREE-FLOW DEVELOPMENT PATCH

Purpose:
The old portal files still contained Firebase Authentication guards. When no Firebase user was logged in, those guards executed location.href="index.html", so a portal opened and immediately returned to the master index.

This patch removes those development-time redirects from the patched modules while keeping the functional Firestore code where possible.

Patched modules included:
- index.html
- admin.html
- announcements.html
- assignments.html
- attendance.html
- course-registration.html
- courses.html
- department.html
- examinations.html
- faculty.html
- fees.html
- lecture-notes.html
- levels.html
- library.html
- payments.html
- programme.html
- reports.html
- results.html
- school-structure.html
- student-profile.html
- student.html
- lecturer.html
- lecturer-profile.html

Important:
This is DEVELOPMENT MODE. Authentication and authorization are intentionally bypassed in these patched pages, matching the current rebuild plan. Do not deploy this version as a production-secure system.

If a different HTML page still returns to index.html, that page contains an authentication/access guard that has not yet been patched. It should be patched in the same development-mode approach.
