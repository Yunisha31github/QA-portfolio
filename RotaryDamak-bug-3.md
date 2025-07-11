# Bug #3: Theme Selection Allows Duplicate Options and More Than Two Entries

**Description:**  
While manually testing the Theme section, I observed that the system allows selecting the same theme (e.g., "National") in both dropdowns and also allows adding more than two themes. This violates the expected behavior that only **one National** and **one International** theme should be added, and only **two total themes** should exist.

**Steps to Reproduce:**  
1. Go to the admin dashboard → Theme section  
2. Click on "Add Theme"  
3. In the first dropdown, select "National"  
4. In the second dropdown, again select "National" (still available)  
5. Submit the form  
6. Add a third theme using the "Add Theme" button

**Expected Result:**  
- Once "National" is selected in one dropdown, it should be **disabled or hidden** in the other  
- The system should **only allow one "National" and one "International"** theme to be submitted  
- After submitting two themes, the **"Add Theme" button** should be **disabled or hidden**

**Actual Result:**  
- I was able to select "National" in both dropdowns  
- I was able to add more than two themes  
- No validation or restriction was applied either on the frontend or backend

**Screenshot:**  
![Bug Screenshot](<attach-screenshot-url-here>)

**Severity:** Medium  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- The dropdown options remained unchanged even after selecting one  
- I could select "National" for both fields without any warning  
- I could add a third theme entry without restriction

**Suggested Fix (for dev team):**  
- Apply logic to **disable already selected options** in the second dropdown  
- Add **backend validation** to ensure only one National and one International theme can be stored  
- After two themes are added, disable or hide the **"Add Theme" button** to prevent further entries
