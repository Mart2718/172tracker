Math 172 Standards Tracker — Supabase edition
Fall 2026 / Section 83301

SETUP
1. Create a new Supabase project in your own account.
2. In Authentication > Users, create one instructor user with your email and a strong password. Keep public sign-ups disabled. Confirm the user exists before the next step.
3. Open the PRIVATE setup.sql file supplied separately. Replace INSTRUCTOR_EMAIL_HERE with the exact email of that user. Run the script in Supabase SQL Editor. It creates a tracker table, enables row-level security, and inserts the class roster. Run it only in your own project. Verify the query found your user: in Table Editor, the trackers table should have one row.
4. From the project Connect dialog, copy the Project URL and publishable key (or find the key under Settings > API Keys). Edit config.js to place those two values between the quotes. Never use the service_role key, database password, or personal password in config.js.
5. Open index.html from a private folder in Chrome or Edge. Sign in. Test one result and reload the page: it should remain saved, and the top status should say Saved to Supabase.
6. If you want to access it from multiple computers, deploy ONLY index.html and config.js to Netlify. Do not publish setup.sql, roster files, or backups. The app files contain no student roster; the database policies permit only your signed-in user to access their tracker.

ENTRY
Choose a standard category, then one of its standards, and enter each student's tier under Attempt 1–4. There is no assessment dropdown or assessment-source prompt. A blank slot means no recorded attempt, while N is a recorded Not yet. The default date is today; change it before entering earlier work. The student view lets you edit an attempt's date and optional source label, and enter points for LRC, Foundational Fluency, and Engagement.

DROPPED STUDENTS
The supplied CSV has no enrollment status column, so none could be identified as dropped automatically. Use Setup & scoring > Archive student to hide a dropped student from active views. Archiving keeps their existing records, and you can restore them later.

SCORING
One attempt receives full tier value: P 100%, C 75%, B 50%, N 0%. With two or more attempts the two highest determine the published anchor-and-confirm score. The 38 standards are weighted equally; unattempted standards count as 0 in the current mastery snapshot. Course grade is mastery 65%, LRC 15%, fluency 10%, engagement 10%. Unentered components count as zero. The displayed course grade is current demonstrated progress, not a final-grade projection.

PRIVACY
Keep setup.sql private: it contains student names. Do not share your login password. The publishable key is designed for browser use; row-level security is what protects the student data. If a save fails, stop entering results until the status returns to Saved to Supabase.
