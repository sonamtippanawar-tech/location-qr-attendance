# Location-Based QR Code Attendance System

### Technologies
HTML (page structure), CSS (design), JavaScript (frontend), Node.js + Express (backend), JSON files (local storage).

### Requirements
Install Node.js 18 or newer.

### Run
1. Extract this ZIP.
2. Open Terminal/Command Prompt in this folder.
3. Run `npm install`
4. Run `npm start`
5. Open `http://localhost:3000`

### Demo accounts
Teacher: `teacher@example.com` / `Teacher@123`
Student: `student@example.com` / `Student@123`

New registrations are student accounts.

### Demo steps
1. Log in as teacher.
2. Click Use my current location while at the classroom, or enter the classroom latitude and longitude.
3. Keep radius at 50 metres (or set 10–500 metres), then generate QR.
4. On a second browser/device, log in as student.
5. Start camera scanner, scan the teacher QR and allow location permission.
6. If within the radius, attendance is recorded. Refresh records to view it.

### Features
Teacher/student login, student registration, server-signed QR expiring in two minutes, camera QR scanner, server-side Haversine distance check, adjustable radius, duplicate-session protection, attendance history, scrypt password hashing and basic security headers.

### Limitations and safety
This is a coursework prototype, not a production attendance system. Browser GPS can be spoofed. The app uses local JSON files and Express's in-memory session store. Production deployment needs HTTPS, a database, persistent sessions, rate limiting, CSRF protection, admin-managed teacher accounts, backups and security testing. Camera and GPS normally require localhost or HTTPS. QR scanner library loads from a CDN and needs internet access.
