#Bug #4: Multiple Past Presidents Allowed for the Same Year

**Description:**  
While manually testing the Past Presidents section, I found that the system allows **adding more than one past president for the same year (e.g., 2010-2011)**. There is no backend validation to prevent duplicate year entries, and all of them are stored in the database.

**Steps to Reproduce:**  
1. Go to the admin dashboard → Past Presidents section  
2. Click on "Add New" or "Upload Past President"  
3. Fill in details and use the year "2010-2011"  
4. Submit the form  
5. Repeat the same process with the same year  
6. Observe the entries in the list or database

**Expected Result:**  
- Only one Past President should be allowed per unique year range  
- The system should reject duplicates with an error like:  
  `"A Past President for this year already exists."`

**Actual Result:**  
- I was able to submit multiple entries with the same year  
- The system did not show any error  
- All duplicate records were stored in the database

**Screenshot:**  
![Bug Screenshot](<attach-screenshot-url-here>)

**Severity:** High  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- I submitted two entries for the same year through the database  
- Both entries were saved and visible in the admin list  
- This may lead to confusion and data inconsistency

**Suggested Fix (for dev team):**  
- Add **backend validation** to ensure each year range is unique  
- Prevent saving a new entry if the year already exists in the database  
- Show a user-friendly message on duplicate submission
