# Dark Mode Feature — Test Cases

**Feature:** Dark Mode  
**Developer:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**App Built:** May 17 – August 9, 2024  
**QA Testing Date:** March–April 2026  

---

## Test Cases

---

### TC-DM-001 — Toggle Dark Mode On

| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-001 |
| **Feature** | Dark Mode |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App is open, dark mode is currently off |

**Steps:**
1. Open the app settings
2. Turn dark mode on

**Expected Result:** Entire app UI switches to dark theme immediately. Background turns dark, text turns light.  
**Actual Result:** Dark mode activated successfully. Background turned dark and text turned light across all visible screens.  
**Status:** ✅ Pass

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
1. Navigate to Settings
2. Turn dark mode off

**Expected Result:** App UI reverts completely to light theme. No dark elements remain.  
**Actual Result:** Light mode restored successfully after toggling off. Note: toggle became unresponsive on first attempt — app restart was required before the toggle responded. See BUG-007.  
**Status:** ✅ Pass (defect noted — BUG-007)

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
**Actual Result:** Dark mode preference was saved and correctly restored after full app restart.  
**Status:** ✅ Pass

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
2. Browse the manga list on the home screen
3. Open a manga detail page and observe cover images

**Expected Result:** Manga cover images are fully visible and readable. No images hidden, distorted, or blending into dark background.  
**Actual Result:** Images were visible during this test session. An intermittent disappearance was observed in a prior session where blank boxes appeared instead of cover images. See BUG-005.  
**Status:** ✅ Pass (intermittent defect noted — BUG-005)

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
1. Enable dark mode in Settings
2. Fully close the app
3. Reopen the app and observe the splash screen on launch

**Expected Result:** Splash screen respects the dark mode setting or transitions smoothly into the dark-themed app.  
**Actual Result:** Splash screen appeared identical in both dark and light mode. Always shows default blue background with red text regardless of theme setting. No dark mode adaptation applied.  
**Status:** ❌ Fail — BUG-008

---

### TC-DM-006 — Switch Dark Mode While Reading

| Field | Details |
|---|---|
| **Test Case ID** | TC-DM-006 |
| **Feature** | Dark Mode |
| **Priority** | Medium |
| **Type** | Functional |
| **Precondition** | User is actively reading a manga chapter |

**Steps:**
1. Open a manga and navigate to the chapter list
2. Select a chapter to open the reader screen
3. Navigate back to Settings without fully closing the reader
4. Toggle dark mode on or off
5. Return to the reader screen and observe

**Expected Result:** Reading screen updates to reflect the new theme. App does not crash or freeze.  
**Actual Result:** Theme was correctly applied when returning to the reader. Text colour and background updated to match the new theme setting. Note: the reader screen has no bottom navigation bar — user must use the back button to exit, making navigation between reader and settings inconvenient to test.  
**Status:** ✅ Pass (navigation usability observation noted)

---

## Test Summary

| Test Case ID | Description | Status | Bugs Linked |
|---|---|---|---|
| TC-DM-001 | Toggle dark mode on | ✅ Pass | — |
| TC-DM-002 | Toggle dark mode off | ✅ Pass | BUG-007 |
| TC-DM-003 | Dark mode persists after restart | ✅ Pass | — |
| TC-DM-004 | Manga images visible in dark mode | ✅ Pass | BUG-005 |
| TC-DM-005 | Dark mode on splash screen | ❌ Fail | BUG-008 |
| TC-DM-006 | Switch dark mode while reading | ✅ Pass | — |

**Pass Rate: 5/6 (83%)**

---

> Testing conducted on Android Studio Emulator — Medium Phone API 34.  
> All bugs linked above are documented in full in bugs-found.md.
