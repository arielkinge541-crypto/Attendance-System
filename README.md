# Attendance System

Real-time attendance system with facial recognition check-in, dashboard, and member enrollment.

## How to use

Open `attendance-system-mockup.html` in a browser (or serve it with GitHub Pages — rename it to `index.html` for that).

- **Dashboard** — live clock, Present / Late / Absent / On Leave counts, weekly chart, records with search and filter.
- **Live Check-In** — opens the camera, frames the face, matches it against enrolled demo members, and asks for confirmation before marking Present. Unknown faces are not marked and cannot check in.
- **Enroll** — name + photo from the camera, for demo members.
- **Simulation buttons** — test a known face and an unknown face when no camera is available.

## Notes

- Demo only: the roster is sample data. All face processing runs in the browser; no face data is saved or sent anywhere.
- The black hexagon logo is Ariel's IT Department logo, shown in the header, check-in screen, and camera screen.
