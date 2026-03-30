# Latest Updates Feature — Test Cases

**Feature:** Latest Updates  
**Developer:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**Date:** March 2026  

---

## Test Cases

### TC-LU-001 — Latest Manga Loads on Home Screen
| Field | Details |
|---|---|
| **Test Case ID** | TC-LU-001 |
| **Feature** | Latest Updates |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Open the app
2. Navigate to the Latest Updates section

**Expected Result:** A list of recently updated manga is displayed with correct titles, cover images and update information.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-LU-002 — Latest Updates Match API Data
| Field | Details |
|---|---|
| **Test Case ID** | TC-LU-002 |
| **Feature** | Latest Updates |
| **Priority** | High |
| **Type** | Integration Testing |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Open the Latest Updates section in the app
2. Note the first 3 manga titles shown
3. Call the MangaVerse API in Postman to fetch latest manga
4. Compare results

**Expected Result:** Manga titles shown in the app match the data returned by the API.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-LU-003 — Latest Updates With No Internet
| Field | Details |
|---|---|
| **Test Case ID** | TC-LU-003 |
| **Feature** | Latest Updates |
| **Priority** | High |
| **Type** | Negative Testing |
| **Precondition** | Device has no internet connection |

**Steps:**
1. Turn off wifi and mobile data
2. Open the app
3. Navigate to Latest Updates section

**Expected Result:** App displays a clear error message such as "No internet connection. Please try again." App does not crash or show a blank screen.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-LU-004 — Loading State for Latest Updates
| Field | Details |
|---|---|
| **Test Case ID** | TC-LU-004 |
| **Feature** | Latest Updates |
| **Priority** | Medium |
| **Type** | UI Testing |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Navigate to Latest Updates section
2. Observe screen immediately before content loads

**Expected Result:** A loading indicator is visible while manga data is being fetched. Screen does not appear frozen or blank.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-LU-005 — Tap a Manga From Latest Updates
| Field | Details |
|---|---|
| **Test Case ID** | TC-LU-005 |
| **Feature** | Latest Updates |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | Latest updates list is loaded |

**Steps:**
1. Open the Latest Updates section
2. Tap on any manga from the list

**Expected Result:** App navigates to the correct manga detail or reading screen. The manga content matches what was tapped.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

## Test Summary

| Test Case ID | Description | Status |
|---|---|---|
| TC-LU-001 | Latest manga loads on home screen | Pending |
| TC-LU-002 | Latest updates match API data | Pending |
| TC-LU-003 | Latest updates with no internet | Pending |
| TC-LU-004 | Loading state for latest updates | Pending |
| TC-LU-005 | Tap a manga from latest updates | Pending |
