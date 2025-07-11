# Bug #1: Invalid Future Date Allowed in "Past President" Upload

**Description:**  
The form for uploading a past president is accepting future dates in the "Date" field, which should not be allowed.

**Steps to Reproduce:**  
1. Go to admin dashboard → Past Presidents section  
2. Click on "Add New" or "Upload Past President"  
3. Enter required details  
4. In the "Date" field, enter a **future date** (e.g., 2026-01-01)  
5. Submit the form

**Expected Result:**  
Form submission should be rejected with an error like:  
`"Date cannot be in the future for a past president."`

**Actual Result:**  
Form is submitted successfully and future-dated record is saved in the database.

**Screenshot:**  
![Bug Screenshot](<attach-screenshot-url-here>)

**Severity:** Medium to High  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Suggested Fix:**  
- Add frontend validation (`max` attribute in `<input type="date">`)  
- Implement backend validation to ensure date is not in the future
