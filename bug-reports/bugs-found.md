# Bug Reports — MangaMania Android App

**Project:** MangaMania  
**Tester:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**App Built:** May 17 – August 9, 2024  
**QA Testing Date:** March–April 2026  

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
| **Critical** | App crashes or core feature is completely broken |
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
**Screenshot:** screenshots/BUG-001.png

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
**Screenshot:** screenshots/BUG-002.png

---

### BUG-003
| Field | Details |
|---|---|
| **Bug ID** | BUG-003 |
| **Title** | Network error message is technical and not user-friendly |
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
**Notes:** Same technical error also appears when genre search is attempted with no internet. The genre search screen itself shows no error message at all — screen stays blank silently.  
**Screenshot:** screenshots/BUG-003.png

---

### BUG-004
| Field | Details |
|---|---|
| **Bug ID** | BUG-004 |
| **Title** | Delete Data feature missing from Settings screen |
| **Feature** | General App |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Open app
2. Tap Settings
3. Look for Delete Data option

**Expected Result:** Delete Data button exists in settings  
**Actual Result:** No Delete Data option found anywhere in settings screen  
**Screenshot:** screenshots/BUG-004.png

---

### BUG-005
| Field | Details |
|---|---|
| **Bug ID** | BUG-005 |
| **Title** | Manga cover images disappear when Dark Mode is enabled (intermittent) |
| **Feature** | Dark Mode |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Open app
2. Go to Settings
3. Enable Dark Mode
4. Go to home screen and browse manga list

**Expected Result:** Manga cover images remain visible in dark mode  
**Actual Result:** Manga cover images intermittently disappear — blank boxes appear where images should be  
**Notes:** Issue is intermittent. Could not reproduce consistently. Documented as observed during session.  
**Screenshot:** screenshots/BUG-005.png

---

### BUG-006
| Field | Details |
|---|---|
| **Bug ID** | BUG-006 |
| **Title** | Categories screen does not apply dark or light theme |
| **Feature** | Dark Mode / Categories |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | New |

**Steps to Reproduce:**
1. Enable dark mode in Settings
2. Navigate to Categories screen

**Expected Result:** Categories screen follows the active dark theme — dark background, light text  
**Actual Result:** Categories screen always shows white background with grey buttons regardless of theme setting  
**Screenshot:** screenshots/BUG-006.png

---

### BUG-007
| Field | Details |
|---|---|
| **Bug ID** | BUG-007 |
| **Title** | Dark Mode toggle becomes unresponsive and requires app restart |
| **Feature** | Dark Mode / Settings |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Go to Settings
2. Tap the Dark Mode toggle multiple times
3. Observe toggle stops responding

**Expected Result:** Toggle responds immediately on every tap and applies the theme change  
**Actual Result:** After multiple taps, the toggle becomes unresponsive. App must be fully restarted for the change to take effect  
**Screenshot:** screenshots/BUG-007.png

---

### BUG-008
| Field | Details |
|---|---|
| **Bug ID** | BUG-008 |
| **Title** | Splash screen does not reflect dark mode setting |
| **Feature** | Dark Mode / Splash Screen |
| **Severity** | Low |
| **Priority** | Low |
| **Status** | New |

**Steps to Reproduce:**
1. Enable dark mode in Settings
2. Fully close the app
3. Reopen the app
4. Observe the splash screen on launch

**Expected Result:** Splash screen adapts to the active dark theme, or transitions smoothly into the dark-themed app  
**Actual Result:** Splash screen appears identical in both dark and light mode — always shows default blue background with red text  
**Screenshot:** screenshots/BUG-008.png

---

### BUG-009
| Field | Details |
|---|---|
| **Bug ID** | BUG-009 |
| **Title** | Manga reader shows blank screen when chapter images fail to load |
| **Feature** | Read / Chapter Viewer |
| **Severity** | Critical |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Open any manga from the home screen
2. Tap READ
3. Select any chapter from the chapter list

**Expected Result:** Manga pages load and display in the reader for reading  
**Actual Result:** Reader screen is completely blank — only gradient background, START AUTO SCROLL button, and back button visible. No manga pages load.  
**Notes:** Reading feature was confirmed working during development between May–August 2024 (last capstone commit August 9, 2024, verified via recorded demo). This is a regression caused by the MangaVerse API returning `{"code":404,"error_message":"chapter not found"}` for chapter IDs no longer available. API content availability changes over time and is outside app control. Root cause confirmed via logcat analysis. The underlying code defect is the absence of error handling — the app should detect the 404 and display a meaningful message rather than a blank screen (see BUG-010).  
**Screenshot:** screenshots/BUG-009.png

---

### BUG-010
| Field | Details |
|---|---|
| **Bug ID** | BUG-010 |
| **Title** | No error message shown to user when chapter content fails to load |
| **Feature** | Error Handling / Read Feature |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Open any manga
2. Tap READ
3. Select any chapter
4. Wait for the reader screen to load

**Expected Result:** If chapter images fail to load, a user-friendly message is shown such as "Chapter not available. Please try another chapter."  
**Actual Result:** Blank screen is displayed with no indication of what went wrong. User has no way to know if the content is loading, unavailable, or if an error occurred.  
**Notes:** Related to BUG-009. The API failure is silent — the app needs error state handling in the reader.  
**Screenshot:** screenshots/BUG-010.png

---

### BUG-011
| Field | Details |
|---|---|
| **Bug ID** | BUG-011 |
| **Title** | Manga title truncated on detail screen |
| **Feature** | UI / Manga Detail Screen |
| **Severity** | Low |
| **Priority** | Low |
| **Status** | New |

**Steps to Reproduce:**
1. Open any manga with a long title (e.g. "I Returned as an FFF-Class Witch Doctor")
2. View the manga detail screen

**Expected Result:** Full manga title is displayed  
**Actual Result:** Title is cut off mid-sentence — e.g. shows "I Returned as an" instead of full title  
**Screenshot:** screenshots/BUG-011.png

---

### BUG-012
| Field | Details |
|---|---|
| **Bug ID** | BUG-012 |
| **Title** | Genre search bar does not filter results by entered genre |
| **Feature** | Search by Genre |
| **Severity** | High |
| **Priority** | High |
| **Status** | New |

**Steps to Reproduce:**
1. Tap the search bar on the home screen
2. Type "fantasy" — note the results
3. Clear and type "action" — note the results
4. Clear and type "harem" — compare results

**Expected Result:** Each genre search returns a distinct set of manga relevant to that specific genre  
**Actual Result:** Results are near-identical across all genre searches. The same manga titles appear regardless of which genre is typed. The search bar input does not change the API query.  
**Notes:** Confirmed via logcat analysis — API call always uses `genres=Harem%2CFantasy%2CAction` regardless of search bar input. The genre search text field appears to be a UI element that is not properly connected to the API filtering logic. Tested with Fantasy, Action, Harem, Adventure, Sci-Fi — all returned overlapping results.  
**Screenshot:** screenshots/BUG-012.png

---

### BUG-013
| Field | Details |
|---|---|
| **Bug ID** | BUG-013 |
| **Title** | Manga detail screen intermittently shows Total Chapters: 0 |
| **Feature** | Latest Updates / Manga Detail |
| **Severity** | Low |
| **Priority** | Low |
| **Status** | New |

**Steps to Reproduce:**
1. Tap LATEST MANGA on home screen
2. Tap any manga from the list
3. Observe the Total Chapters field on the detail screen

**Expected Result:** Total Chapters displays the correct number of chapters available for the selected manga  
**Actual Result:** Some manga show "Total Chapters: 0" despite having chapters available. Confirmed on Re:Zero kara Hajimeru and Hell Warden Higuma during testing. Other manga in the same session displayed correct chapter counts.  
**Notes:** Issue is intermittent. Likely caused by inconsistent chapter count data in the MangaVerse API response for certain manga entries. Could not reproduce consistently across all manga. Documented as observed.  
**Screenshot:** screenshots/BUG-013.png

---

### BUG-014
| Field | Details |
|---|---|
| **Bug ID** | BUG-014 |
| **Title** | App takes approximately 10 seconds to fully load on launch |
| **Feature** | General / Performance |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | New |

**Steps to Reproduce:**
1. Fully close the app
2. Tap the app icon to launch
3. Time from tap until home screen manga cards are fully visible

**Expected Result:** App fully loads within 3 seconds  
**Actual Result:** App takes approximately 10 seconds to fully load. Splash screen plays but home screen manga cards take significant time to appear. Likely caused by API call on startup fetching manga data before rendering.  
**Screenshot:** screenshots/BUG-014.png

---

## Bug Summary

| Bug ID | Title | Feature | Severity | Status |
|---|---|---|---|---|
| BUG-001 | Duplicate bookmarks created | Bookmark | High | New |
| BUG-002 | No way to remove individual bookmarks | Bookmark | High | New |
| BUG-003 | Technical network error message | General App | Medium | New |
| BUG-004 | Delete Data feature missing | General App | High | New |
| BUG-005 | Manga images disappear in Dark Mode (intermittent) | Dark Mode | High | New |
| BUG-006 | Categories screen ignores dark/light theme | Dark Mode | Medium | New |
| BUG-007 | Dark Mode toggle becomes unresponsive | Dark Mode | High | New |
| BUG-008 | Splash screen does not reflect dark mode | Dark Mode | Low | New |
| BUG-009 | Manga reader shows blank screen on 404 | Read Feature | Critical | New |
| BUG-010 | No error message when chapter fails to load | Error Handling | High | New |
| BUG-011 | Manga title truncated on detail screen | UI | Low | New |
| BUG-012 | Genre search bar does not filter by genre | Search by Genre | High | New |
| BUG-013 | Total Chapters shows 0 on detail screen (intermittent) | Latest Updates | Low | New |
| BUG-014 | App takes ~10 seconds to fully load on launch | General / Performance | Medium | New |

---

> Screenshots stored in /screenshots folder and linked per bug.  
> Bugs will be logged into Jira after manual testing is complete.
