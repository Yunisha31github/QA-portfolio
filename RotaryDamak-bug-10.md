# Bug #10: Past Event Allows Future Date

**Description:**  
During manual testing, I observed that the system allows submiting on the Past Event section while selecting a **future date**, which is logically incorrect. A past event should only accept dates that are in the past or today, not in the future.

**Steps to Reproduce:**  
1. Go to the admin dashboard →Past Events section  
2. Click on "Add New Event"  
3. Select a **future date** (e.g., 2026-01-01) as the event date  
4. Submit the form

**Expected Result:**  
- The form should be rejected with an error like:  
  `"Past events cannot have future dates."`  
- Date picker should restrict future selection when submiting on past event in database

**Actual Result:**  
- The system allows submission of a "Past" event with a future date  
- The record is saved and displayed as a past event scheduled in the future

**Screenshot:**  
![Bug Screenshot](<./bugScreenshots/pastevent.PNG>)

**Severity:** Medium to High  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- No date restriction applied when submiting in past event section with future dates 
- Could lead to confusion in the events list for users and admins

**Suggested Fix (for dev team):**  
- The past event date must be **today or earlier**  
- Disable future dates from the date picker
- Add a backend check to enforce the rule even if bypassed on frontend
