# Search by Genre Feature — Test Cases

**Feature:** Search by Genre  
**Developer:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**Date:** March 2026  

---

## Test Cases

### TC-GS-001 — Select a Valid Genre
| Field | Details |
|---|---|
| **Test Case ID** | TC-GS-001 |
| **Feature** | Search by Genre |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Navigate to the genre search screen
2. Select any available genre (e.g. Action, Romance, Horror)
3. Wait for results to load

**Expected Result:** A list of manga matching the selected genre is displayed. Results are relevant to the selected genre.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GS-002 — Genre Results Match API Data
| Field | Details |
|---|---|
| **Test Case ID** | TC-GS-002 |
| **Feature** | Search by Genre |
| **Priority** | High |
| **Type** | Integration Testing |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Select a genre in the app
2. Note the manga titles displayed
3. Call the MangaVerse API directly in Postman with the same genre parameter
4. Compare results

**Expected Result:** Manga displayed in the app matches the data returned by the API for that genre.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GS-003 — Genre With No Results
| Field | Details |
|---|---|
| **Test Case ID** | TC-GS-003 |
| **Feature** | Search by Genre |
| **Priority** | Medium |
| **Type** | Negative Testing |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Navigate to genre search
2. Select or enter a genre that returns no results

**Expected Result:** An empty state message is displayed such as "No manga found for this genre". App does not crash or show a blank screen.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GS-004 — Genre Search With No Internet
| Field | Details |
|---|---|
| **Test Case ID** | TC-GS-004 |
| **Feature** | Search by Genre |
| **Priority** | High |
| **Type** | Negative Testing |
| **Precondition** | Device has no internet connection |

**Steps:**
1. Turn off wifi and mobile data
2. Open the app
3. Navigate to genre search
4. Select any genre

**Expected Result:** App displays an error message such as "No internet connection". App does not crash or freeze.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GS-005 — Loading State While Fetching Genre Results
| Field | Details |
|---|---|
| **Test Case ID** | TC-GS-005 |
| **Feature** | Search by Genre |
| **Priority** | Medium |
| **Type** | UI Testing |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Select a genre
2. Observe the screen immediately after selecting before results load

**Expected Result:** A loading indicator such as a spinner or progress bar is visible while results are being fetched from the API.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GS-006 — Switch Between Different Genres
| Field | Details |
|---|---|
| **Test Case ID** | TC-GS-006 |
| **Feature** | Search by Genre |
| **Priority** | Medium |
| **Type** | Functional |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Select Genre A and wait for results
2. Go back and select Genre B
3. Wait for results

**Expected Result:** Results update correctly to show Genre B manga. No results from Genre A remain visible. App does not crash.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

## Test Summary

| Test Case ID | Description | Status |
|---|---|---|
| TC-GS-001 | Select a valid genre | Pending |
| TC-GS-002 | Genre results match API data | Pending |
| TC-GS-003 | Genre with no results | Pending |
| TC-GS-004 | Genre search with no internet | Pending |
| TC-GS-005 | Loading state while fetching | Pending |
| TC-GS-006 | Switch between different genres | Pending |
