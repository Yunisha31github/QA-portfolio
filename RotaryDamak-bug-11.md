# Bug #11: Footer "About Us" Text Misplaced on Normal Screen

**Description:**  
While viewing the website on a **standard screen resolution**, the **text inside the "About Us" section** of the footer appears **misplaced or overlapping** with the adjacent "END POLIO NOW" banner image. The layout does not look clean or properly spaced.

**Steps to Reproduce:**  
1. Open the website on a standard desktop screen (e.g., 1366×768 or 1920×1080)  
2. Scroll to the footer section  
3. Observe the alignment of the "About Us" text

**Expected Result:**  
- The "About Us" text should be properly aligned to the right of the image  
- There should be consistent spacing between the image and the text  
- Text should not appear over the image or too close to it

**Actual Result:**  
- The text overlaps or sits awkwardly near the "END POLIO NOW" banner  
- The layout appears broken and not visually clean

**Screenshot:**  
![Bug Screenshot](<./bugScreenshots/footer.PNG>)

**Severity:** Medium (Visual/UI Issue)  
**Tools Used:** Chrome DevTools, Standard Browser  
**Status:** Open (Reported)

**Notes from Manual Testing:**  
- The issue appears on common screen widths, not just mobile  
- Likely caused by improper flex or float alignment, or missing padding/margin

**Suggested Fix (for dev team):**  
- Use CSS layout properties (like `flex`, `grid`, or `float`) properly to separate image and text  
- Apply margin or padding to keep spacing consistent  
- Ensure columns are aligned using a layout wrapper or container
