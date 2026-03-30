# Bookmark Feature — Test Cases

**Feature:** Bookmark  
**Developer:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**Date:** March 2026  

---

## Test Cases

### TC-BM-001 — Bookmark a Single Manga
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-001 |
| **Feature** | Bookmark |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App is open, user is on manga list screen |

**Steps:**
1. Browse the manga list
2. Tap on any manga to open it
3. Tap the bookmark icon

**Expected Result:** Manga is saved to bookmarks list. Bookmark icon changes state (filled/highlighted).  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-BM-002 — Bookmarked Manga Appears in Saved List
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-002 |
| **Feature** | Bookmark |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | At least one manga has been bookmarked |

**Steps:**
1. Bookmark a manga
2. Navigate to the Bookmarks section
3. Verify the bookmarked manga appears in the list

**Expected Result:** The bookmarked manga is visible in the bookmarks list with correct title and image.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-BM-003 — Bookmark Same Manga Twice
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-003 |
| **Feature** | Bookmark |
| **Priority** | Medium |
| **Type** | Negative Testing |
| **Precondition** | A manga is already bookmarked |

**Steps:**
1. Open a manga that is already bookmarked
2. Tap the bookmark icon again

**Expected Result:** The manga is either removed from bookmarks (toggle behavior) OR a message appears saying it is already bookmarked. No duplicate entry is created.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-BM-004 — Remove a Bookmark
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-004 |
| **Feature** | Bookmark |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | At least one manga is bookmarked |

**Steps:**
1. Navigate to the Bookmarks section
2. Find a bookmarked manga
3. Tap the remove/unbookmark option

**Expected Result:** Manga is immediately removed from the bookmarks list. List updates without requiring a refresh.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-BM-005 — Bookmarks Persist After App Restart
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-005 |
| **Feature** | Bookmark |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | At least one manga is bookmarked |

**Steps:**
1. Bookmark one or more manga
2. Fully close the app
3. Reopen the app
4. Navigate to Bookmarks section

**Expected Result:** All previously bookmarked manga are still present in the list after restart.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-BM-006 — Bookmark With No Internet Connection
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-006 |
| **Feature** | Bookmark |
| **Priority** | Medium |
| **Type** | Negative Testing |
| **Precondition** | App is open, device has no internet connection |

**Steps:**
1. Turn off wifi and mobile data on the device/emulator
2. Open a manga from a previously loaded list
3. Tap the bookmark icon

**Expected Result:** Bookmark is saved locally and a success message is shown. App does not crash.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-BM-007 — Bookmark List Empty State
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-007 |
| **Feature** | Bookmark |
| **Priority** | Low |
| **Type** | UI Testing |
| **Precondition** | No manga has been bookmarked |

**Steps:**
1. Open the app fresh with no bookmarks
2. Navigate to the Bookmarks section

**Expected Result:** A message such as "No bookmarks yet" or similar empty state is displayed. Screen does not show a blank or broken UI.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-BM-008 — Bookmark Count After Delete All Data
| Field | Details |
|---|---|
| **Test Case ID** | TC-BM-008 |
| **Feature** | Bookmark + Delete Data |
| **Priority** | Medium |
| **Type** | Integration Testing |
| **Precondition** | Multiple manga are bookmarked |

**Steps:**
1. Bookmark 3 or more manga
2. Navigate to settings
3. Use the "Delete Data" feature to clear all stored data
4. Navigate back to the Bookmarks section

**Expected Result:** Bookmarks list is completely empty after deleting all data.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

## Test Summary

| Test Case ID | Description | Status |
|---|---|---|
| TC-BM-001 | Bookmark a single manga | Pending |
| TC-BM-002 | Bookmarked manga appears in saved list | Pending |
| TC-BM-003 | Bookmark same manga twice | Pending |
| TC-BM-004 | Remove a bookmark | Pending |
| TC-BM-005 | Bookmarks persist after app restart | Pending |
| TC-BM-006 | Bookmark with no internet | Pending |
| TC-BM-007 | Bookmark list empty state | Pending |
| TC-BM-008 | Bookmark count after delete all data | Pending |
