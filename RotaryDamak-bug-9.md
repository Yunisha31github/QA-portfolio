# bug #9: Event End Date Allows Earlier Date Than Start Date

**Description:**  
While testing the Event form, I found that the system allows entering an **end date that is earlier than the start date**. This is a logical error — an event cannot end before it starts, and proper validation is missing.

**Steps to Reproduce:**  
1. Go to the admin dashboard → Events section  
2. Click on "Add New Event"  
3. Set the **start date** (e.g., 2024-08-10)  
4. Set the **end date** earlier than the start date (e.g., 2024-08-09)  
5. Submit the form

**Expected Result:**  
- The form should be **rejected** with a message like:  
  `"End date must be the same or after the start date."`

**Actual Result:**  
- The form submits successfully  
- The invalid event is stored in the database without any error or warning

**Screenshot:**  
![Bug Screenshot](<./bugScreenshots/eventvalidation.PNG>)

**Severity:** High  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- No client-side or server-side validation appears to check date logic  
- Could lead to incorrect event scheduling and confusion for users

**Suggested Fix (for dev team):**  
- Add validation to **prevent submission if end date is earlier than start date**  
- Apply the check on both **frontend (UI form validation)** and **backend (before saving to DB)**
