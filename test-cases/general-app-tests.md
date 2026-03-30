# General App — Test Cases

**Feature:** General App Behaviour & Navigation  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**Date:** March 2026  

---

## Test Cases

### TC-GA-001 — App Launch Time
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-001 |
| **Feature** | General |
| **Priority** | High |
| **Type** | Performance Testing |
| **Precondition** | App is installed on device or emulator |

**Steps:**
1. Close the app completely
2. Tap the app icon to launch
3. Measure time until the home screen is fully loaded

**Expected Result:** App fully loads within 3 seconds. Splash screen animation plays smoothly.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GA-002 — App Behaviour With Slow Internet
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-002 |
| **Feature** | General |
| **Priority** | High |
| **Type** | Negative Testing |
| **Precondition** | App is open, internet is throttled to slow speed |

**Steps:**
1. Set emulator network speed to slow (2G or throttled)
2. Navigate through the app
3. Try loading manga list and images

**Expected Result:** App shows loading indicators while waiting. Does not crash or freeze. Content eventually loads or shows a timeout message.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GA-003 — App Behaviour With No Internet
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-003 |
| **Feature** | General |
| **Priority** | High |
| **Type** | Negative Testing |
| **Precondition** | Device has no internet connection |

**Steps:**
1. Turn off all network connections
2. Launch the app
3. Navigate to multiple screens

**Expected Result:** App displays appropriate error messages on each screen. Does not crash. Offline-compatible features like bookmarks still function.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GA-004 — Back Button Navigation
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-004 |
| **Feature** | General |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App is open |

**Steps:**
1. Navigate from home screen to manga list
2. Open a manga detail screen
3. Press the back button
4. Press back again
5. Continue pressing back through all screens

**Expected Result:** Each back button press navigates to the previous screen in the correct order. No screens are skipped or repeated. App exits cleanly when back is pressed from the home screen.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GA-005 — Delete All Data Feature
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-005 |
| **Feature** | General / Delete Data |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App has stored data including bookmarks and favourites |

**Steps:**
1. Add bookmarks and favourites
2. Navigate to settings
3. Tap "Delete Data" with a single click
4. Confirm the action if prompted
5. Check bookmarks, favourites and all stored data

**Expected Result:** All stored data is completely cleared in one action. Bookmarks list and favourites are empty. App does not crash.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GA-006 — Interactive Tutorial on First Launch
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-006 |
| **Feature** | General / Tutorial |
| **Priority** | Medium |
| **Type** | Functional |
| **Precondition** | App is freshly installed with no prior data |

**Steps:**
1. Install and launch the app for the first time
2. Observe if tutorial appears automatically
3. Follow through all tutorial steps

**Expected Result:** Tutorial launches automatically on first use. All navigation steps are clear and functional. Tutorial can be completed without errors.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GA-007 — Dark Mode and Bookmark Used Together
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-007 |
| **Feature** | General / Integration |
| **Priority** | Medium |
| **Type** | Integration Testing |
| **Precondition** | App is open |

**Steps:**
1. Enable dark mode
2. Browse manga list
3. Bookmark several manga
4. Navigate to bookmarks section

**Expected Result:** Bookmarks screen displays correctly in dark mode. All bookmarked manga appear with correct dark theme styling. No UI conflicts between features.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-GA-008 — App on Different Screen Sizes
| Field | Details |
|---|---|
| **Test Case ID** | TC-GA-008 |
| **Feature** | General / UI |
| **Priority** | Medium |
| **Type** | UI Testing |
| **Precondition** | Android Studio emulator available with multiple device profiles |

**Steps:**
1. Run the app on a small screen emulator (e.g. Pixel 4)
2. Check all major screens
3. Run the app on a large screen emulator (e.g. Pixel 7 Pro)
4. Check all major screens again

**Expected Result:** UI scales correctly on both screen sizes. No text is cut off, no buttons are hidden, no layout is broken on either device.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

## Test Summary

| Test Case ID | Description | Status |
|---|---|---|
| TC-GA-001 | App launch time | Pending |
| TC-GA-002 | App behaviour with slow internet | Pending |
| TC-GA-003 | App behaviour with no internet | Pending |
| TC-GA-004 | Back button navigation | Pending |
| TC-GA-005 | Delete all data feature | Pending |
| TC-GA-006 | Interactive tutorial on first launch | Pending |
| TC-GA-007 | Dark mode and bookmark used together | Pending |
| TC-GA-008 | App on different screen sizes | Pending |
