# PRODIGY_ST_02
Test case 2
Test a simple web page across different browsers (e.g. chrome, firefox, safari, Edge) and devices (e.g. desktop, tablet, mobile).Check for the layout issues, broken links and functionality discrepancies. 

# Compatibility Test Plan  
**Project:** E-Commerce Demo Website  
**Test Type:** Cross-Browser & Cross-Device Compatibility  
**Tester:** sweta kumari 
**Date:** 2025-07-04  

---

## **1. Test Objectives**  
Verify the web page functions consistently across:  
- **Browsers:** Chrome, Firefox, Safari, Edge  
- **Devices:** Desktop (Windows/macOS), Tablet (iPad), Mobile (iPhone/Android)  

---

## **2. Test Setup**  
### **Tools Required:**  
- BrowserStack/LambdaTest (or manual testing on physical devices).  
- Chrome DevTools (for device emulation).  
- W3C Validator (for code checks).  

### **Test URLs:**  
- Homepage: `https://demo-ecom-site.com`  
- Product Page: `https://demo-ecom-site.com/products`  

---

## **3. Test Cases**  
### **3.1 Layout & Responsiveness**  
#### **TC-01: Homepage Layout Consistency**  
**Steps:**  
1. Open the homepage on Chrome, Firefox, Safari, and Edge.  
2. Compare element alignment (header, footer, product grid).  
**Expected:** No misaligned elements or overlapping text.  

#### **TC-02: Mobile Responsiveness**  
**Steps:**  
1. Use DevTools to simulate iPhone 12 and Pixel 5.  
2. Check if:  
   - Text scales without horizontal scrolling.  
   - Images resize proportionally.  
**Expected:** Fully responsive on mobile.  

---

### **3.2 Functionality**  
#### **TC-03: Product Search**  
**Steps:**  
1. Enter "laptop" in the search bar.  
2. Press "Enter" on each browser.  
**Expected:** Results load identically across browsers.  

#### **TC-04: Add to Cart**  
**Steps:**  
1. Click "Add to Cart" on a product.  
2. Verify cart icon updates.  
**Expected:** Cart count increments without JavaScript errors.  

---

### **3.3 Cross-Browser Checks**  
#### **TC-05: Form Submission**  
**Steps:**  
1. Fill the checkout form with test data.  
2. Submit on each browser.  
**Expected:** Success message appears; no browser-specific errors.  

#### **TC-06: Media Loading**  
**Steps:**  
1. Check product images/videos on Safari (iOS) and Chrome (Android).  
**Expected:** No broken images/videos.  

---

## **4. Defect Reporting**  
### **Bug Report Template:**  
```markdown
**Bug ID:** #001  
**Title:** Menu overlap on Safari iOS  
**Description:** Navigation menu items overlap on iPhone 12 (Safari 16+).  
**Steps to Reproduce:**  
1. Open homepage on Safari (iOS).  
2. Click hamburger menu.  
**Expected:** Clean dropdown menu.  
**Actual:** Text overlaps due to `padding` issue.  
**Priority:** High  

Test Results Summary

Test Case	 Pass/Fail	Affected Browser/Device	  Remarks
TC-01	     Pass	      All	                      -
TC-02	     Fail	      Safari (iOS)	            Menu overlap
TC-03	     Pass	      All	                      -

Recommendations
Fix CSS padding for Safari iOS menus.
Test payment gateway on Edge (known rendering lag).
Optimize image loading for mobile data speeds.
