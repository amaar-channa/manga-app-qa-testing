# Dark Mode Feature — Test Cases

**Feature:** Dark Mode  
**Developer:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**Date:** March 2026  

---

## Test Cases

### TC-DM-001 — Toggle Dark Mode On
| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-001 |
| **Feature** | Dark Mode |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App is open, dark mode is currently off |

**Steps:**
1. Open the app settings or toggle location
2. Turn dark mode on

**Expected Result:** Entire app UI switches to dark theme immediately. Background turns dark, text turns light.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-DM-002 — Toggle Dark Mode Off
| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-002 |
| **Feature** | Dark Mode |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | Dark mode is currently on |

**Steps:**
1. Navigate to settings or toggle location
2. Turn dark mode off

**Expected Result:** App UI reverts completely to light theme. No dark elements remain.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-DM-003 — Dark Mode Persists After App Restart
| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-003 |
| **Feature** | Dark Mode |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | Dark mode is enabled |

**Steps:**
1. Enable dark mode
2. Fully close the app
3. Reopen the app

**Expected Result:** App reopens in dark mode. User preference is saved and restored correctly.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-DM-004 — Manga Images Visible in Dark Mode
| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-004 |
| **Feature** | Dark Mode |
| **Priority** | Medium |
| **Type** | UI Testing |
| **Precondition** | Dark mode is enabled |

**Steps:**
1. Enable dark mode
2. Browse the manga list
3. Open a manga and read several pages

**Expected Result:** Manga images are fully visible and readable. No images are hidden, distorted or blending into dark background.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-DM-005 — Dark Mode on Splash Screen
| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-005 |
| **Feature** | Dark Mode |
| **Priority** | Low |
| **Type** | UI Testing |
| **Precondition** | Dark mode is enabled |

**Steps:**
1. Enable dark mode
2. Fully close the app
3. Reopen the app and observe the splash screen

**Expected Result:** Splash screen respects the dark mode setting or transitions smoothly into the dark themed app.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

### TC-DM-006 — Switch Dark Mode While Reading
| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-006 |
| **Feature** | Dark Mode |
| **Priority** | Medium |
| **Type** | Functional |
| **Precondition** | User is actively reading a manga page |

**Steps:**
1. Open a manga and start reading
2. Without closing the reader, toggle dark mode on or off

**Expected Result:** Reading screen updates immediately to reflect the new theme. App does not crash or freeze.  
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

## Test Summary

| Test Case ID | Description | Status |
|---|---|---|
| TC-DM-001 | Toggle dark mode on | Pending |
| TC-DM-002 | Toggle dark mode off | Pending |
| TC-DM-003 | Dark mode persists after restart | Pending |
| TC-DM-004 | Manga images visible in dark mode | Pending |
| TC-DM-005 | Dark mode on splash screen | Pending |
| TC-DM-006 | Switch dark mode while reading | Pending |
