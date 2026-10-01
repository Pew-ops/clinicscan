# ClinicScan (phone-first)
Scan a student ID with the phone camera -> ID number, name and date are filled in -> Save -> Download Excel
(columns: student id, student name, date availed; all values stored as text, date as YYYY-MM-DD).

## Deploy on Vercel
Option A (no install): push this folder to a GitHub repo -> vercel.com -> Add New Project -> import the repo -> Deploy.
Option B (CLI): `npx vercel --prod` inside this folder.
Open the Vercel link on your phone (HTTPS is required for the camera), then "Add to Home Screen".

## Notes
- OCR (Tesseract.js) runs in the browser; ID photos are never uploaded or stored.
- Names are learned after a student's first visit, or import an Excel/CSV (student id, student name) in the Students tab.
- Data is stored on that phone (localStorage). Download the Excel regularly. For many devices at once, a backend is needed.
