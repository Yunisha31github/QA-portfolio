# Bug #6: Missing Validation for Name, Phone & Duplicate Designation Assignment

**Description:**  
While manually testing the Board Members section on database, I found that the system lacks proper validation for both **name** and **phone number fields** — they accept invalid input. Additionally, **designations like "President" can be assigned to multiple members**, which should not be allowed. These issues result in data inconsistency and incorrect board structure.

**Steps to Reproduce:**  
1. Go to the admin dashboard -> Board Members section  
2. Click on "Add Member"  
3. Type invalid(symbols in name, more than 10 numbers on phone number) input in the name and phone number field 
4. Assign the "President" role to a member and submit  
5. Repeat and assign "President" again to another member  
6. Check database or frontend display

**Expected Result:**  
- Name and phone number fields should be **required and validated** (e.g., only valid 10-digit numbers)  
- Designations like "President" should be **unique** — only one member should be allowed to hold it  
- If a designation is already used, the system should show an error like:  
  `"President position is already assigned."`

**Actual Result:**  
- I was able to submit the form with invalid name/phone number  
- I assigned "President" to **multiple members**, and all were saved successfully  
- No error or warning was shown for any of these issues

**Screenshot:**  
![Bug Screenshot](<./bugScreenshots/boardmember validation.PNG>)
![Bug Screenshot](<./bugScreenshots/multiplepresident.jpeg>)

**Severity:** High  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- Validation is missing on the server sides  
- Form does not restrict role duplication  
- Can lead to confusion in board listings and poor data quality

**Suggested Fix (for dev team):**  
- Add **required field validation** for name and phone number (with regex for valid phone format)  
- Implement **backend checks** to ensure each designation is **unique**  
- Disable or remove a designation from the dropdown once assigned to someone
