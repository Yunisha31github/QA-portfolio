# Bug #5: Board Members Not Sorted by Position in UI

**Description:**  
While testing the Board Members display section, I noticed that members are shown based on the **order they were added to the database**, not by their **assigned position** (e.g., President, Vice President, Member). This leads to an incorrect and unprofessional presentation of leadership hierarchy.

**Steps to Reproduce:**  
1. Go to the Board Members section on the admin panel  
2. Add multiple members with different positions (e.g., President, Member, Treasurer)  
3. View the frontend list of board members

**Expected Result:**  
- Board members should appear in the UI in a **logical order of positions** (e.g., President first, then Vice President, Secretary, Members, etc.)

**Actual Result:**  
- Board members appear in the order they were **added**, not according to their **position**

**Screenshot:**  
![Bug Screenshot](<./bugScreenshots/board_member_issues.PNG>)

**Severity:** Medium  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- I verified the display order multiple times after changing the sequence in the database  
- No sorting logic based on position seems to be applied in the frontend rendering

**Suggested Fix (for dev team):**  
- Apply sorting on the backend or frontend to display members based on **predefined role hierarchy**  
- Optionally create a **position priority system** (e.g., 1 = President, 2 = VP, etc.) to sort accurately
