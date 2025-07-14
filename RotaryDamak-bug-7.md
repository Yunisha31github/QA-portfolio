# Bug #7: 404 Error Thrown on Routes Other Than Home

**Description:**  
While testing navigation in the web application, I found that accessing **any route other than the Home page** (e.g., `/about`, `/contact`, `/board-members`) results in a **404 Page Not Found** error. This indicates improper routing configuration, especially when accessing routes directly via the browser or page refresh.

**Steps to Reproduce:**  
1. Open the application (e.g., `https://rotarysite.com`)  
2. Click on or manually enter a route like `/about` or `/board-members`  
3. Press Enter or refresh the page

**Expected Result:**  
- The correct component or page for the route should load without error  
- No 404 error should be shown for valid, existing routes

**Actual Result:**  
- A 404 error page is shown for all routes except `/` (Home)  
- Pages cannot be accessed via direct link or refresh

**Severity:** High  
**Tools Used:** Trello, Chrome DevTools  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- Issue appears when directly typing or refreshing a non-home route  
- Likely due to missing fallback handling or server-side routing mismatch

