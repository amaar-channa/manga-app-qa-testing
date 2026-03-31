# Bug Reports — MangaMania Android App

**Project:** MangaMania  
**Tester:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**Date:** March 2026  

---

## Bug Report Template

Each bug found during testing is documented below using the following format:

| Field | Description |
|---|---|
| **Bug ID** | Unique identifier for the bug |
| **Title** | Short descriptive title |
| **Feature** | Which feature the bug belongs to |
| **Severity** | Critical / High / Medium / Low |
| **Priority** | High / Medium / Low |
| **Status** | New / In Progress / Fixed / Verified / Closed |
| **Steps to Reproduce** | Exact steps to trigger the bug |
| **Expected Result** | What should happen |
| **Actual Result** | What actually happens |
| **Screenshot** | Attached if available |

---

## Severity Definitions

| Severity | Meaning |
|---|---|
| **Critical** | App crashes or data is lost |
| **High** | Major feature is broken or unusable |
| **Medium** | Feature works but behaves incorrectly |
| **Low** | Minor UI issue or cosmetic problem |

---

## Bugs Found

---

### BUG-001
| Field | Details |
|---|---|
| **Bug ID** | BUG-001 |
| **Title** | Bookmarking same manga multiple times creates duplicate entries |
| **Feature** | Bookmark |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Open any manga
2. Tap BOOKMARK
3. Go back
4. Open same manga again
5. Tap BOOKMARK again
6. Check favourites list

**Expected Result:** App prevents duplicate — shows message or toggles bookmark off  
**Actual Result:** Same manga added again as a new duplicate entry every time BOOKMARK is tapped  
**Screenshot:** 

---

### BUG-002
| Field | Details |
|---|---|
| **Bug ID** | BUG-002 |
| **Title** | No way to remove individual bookmarks from favourites list |
| **Feature** | Bookmark |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Bookmark any manga
2. Navigate to favourites screen
3. Long press or swipe on any bookmarked manga

**Expected Result:** A remove or delete option appears  
**Actual Result:** Nothing happens — no way to remove individual bookmarks  
**Screenshot:** 

---

### BUG-003
| Field | Details |
|---|---|
| **Bug ID** | BUG-003 |
| **Title** | Network error message is technical and not user friendly |
| **Feature** | General App |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | New |

**Steps to Reproduce:**
1. Turn off internet connection
2. Open the app
3. Wait for error message to appear

**Expected Result:** A friendly message like "No internet connection. Please check your network and try again."  
**Actual Result:** Technical error shown: "Failed to fetch manga: Unable to resolve host 'mangaverse-api.p.rapidapi.com'"  
**Screenshot:** 

---

### BUG-004
| Field | Details |
|---|---|
| **Bug ID** | BUG-004 |
| **Title** | Delete Data feature missing from Settings screen |
| **Feature** | General App / Delete Data |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Open app
2. Tap Settings
3. Look for Delete Data option

**Expected Result:** Delete Data button exists in settings  
**Actual Result:** No Delete Data option found anywhere in settings screen  
**Screenshot:** 

---

### BUG-005
| Field | Details |
|---|---|
| **Bug ID** | BUG-005 |
| **Title** | Manga cover images disappear when Dark Mode is enabled |
| **Feature** | Dark Mode |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Open app
2. Go to Settings
3. Enable Dark Mode
4. Go to home screen

**Expected Result:** Manga cover images remain visible  
**Actual Result:** All manga cover images disappear, only titles show, blank white boxes appear  
**Screenshot:** 

---

## Bug Summary

| Bug ID | Title | Feature | Severity | Status |
|---|---|---|---|---|
| BUG-001 | Duplicate bookmarks created | Bookmark | High | New |
| BUG-002 | No way to remove individual bookmarks | Bookmark | High | New |
| BUG-003 | Technical network error message | General App | Medium | New |
| BUG-004 | Delete Data feature missing | General App | High | New |
| BUG-005 | Manga images disappear in Dark Mode | Dark Mode | High | New |

---

> Bug reports will be updated after manual testing session is complete.  
> Screenshots will be added to the /screenshots folder and linked here.
