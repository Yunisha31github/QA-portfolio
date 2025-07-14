#Bug #8: Multiple Welcome Messages Allowed — Button Should Disable After One

**Description:**  
While manually testing the Welcome Message section, I observed that the system allows **adding multiple welcome messages**, even though only **one** should be allowed. There is no restriction or validation preventing duplicate entries, and the **"Add Welcome Message"** button remains active even after one message is submitted.

**Steps to Reproduce:**  
1. Go to the admin dashboard → Welcome Message section  
2. Click on "Add Welcome Message"  
3. Enter and submit the welcome message  
4. Click "Add Welcome Message" again  
5. Submit another message

**Expected Result:**  
- Only one welcome message should be allowed in the database  
- After adding the first message, the **"Add Welcome Message"** button should be **disabled or hidden**  
- System should show a message like:  
  `"Only one welcome message is allowed. Please edit the existing one."`

**Actual Result:**  
- I was able to add multiple welcome messages while we only need one welcome message to show on UI 
- All were saved in the database  
- No error or restriction was triggered

**📸 Screenshot:**  
![Bug Screenshot](<./bugScreenshots/welcome message bug.PNG>)

**Severity:** Medium  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- The database did not check for existing welcome message  
- No warning or prevention logic applied on database

**Suggested Fix (for dev team):**  
- Add **backend validation** to prevent insertion if a welcome message already exists  
- After adding one message, **disable** or **hide** the "Add Welcome Message" button in the database  
  
