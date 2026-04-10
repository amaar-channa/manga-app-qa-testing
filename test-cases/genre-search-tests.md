# Search by Genre Feature — Test Cases

**Feature:** Search by Genre  
**Developer:** Amaar Yasir Channa  
**Platform:** Android  
**Tested On:** Android Studio Emulator  
**App Built:** May 17 – August 9, 2024  
**QA Testing Date:** March–April 2026  

---

## Test Cases

---

### TC-GS-001 — Select a Valid Genre

| Field | Details |
|---|---|
| **Test Case ID** | TC-GS-001 |
| **Feature** | Search by Genre |
| **Priority** | High |
| **Type** | Functional |
| **Precondition** | App is open, internet connection is active |

**Steps:**
1. Navigate to the home screen
2. Tap CATEGORIES
3. Select any available genre (e.g. Action, Fantasy, Harem)
4. Wait for results to load

**Expected Result:** A list of manga matching the selected genre is displayed. Results are relevant to the selected genre.  
**Actual Result:** Tapped CATEGORIES — categories screen opened showing 5 genre buttons: Fantasy, Action, Harem, Adventure, Sci-Fi. Tapped Action — manga list loaded successfully with cover images and titles visible.  
**Status:** ✅ Pass

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
1. Select a genre in the app (e.g. Fantasy)
2. Note the manga titles displayed
3. Select a different genre (e.g. Action)
4. Compare results between genres

**Expected Result:** Each genre returns a distinct set of manga relevant to that specific genre. Results differ meaningfully between genres.  
**Actual Result:** Results were near-identical across all genres tested (Fantasy, Action, Harem, Adventure). The same manga titles appeared regardless of which genre was selected. Confirmed via logcat — API call always uses `genres=Harem%2CFantasy%2CAction` regardless of user input. The genre selection does not change the API query.  
**Status:** ❌ Fail — BUG-012

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
2. Type a genre that is not supported by the app (e.g. "Romance", "Horror")

**Expected Result:** An empty state message is displayed such as "No manga found for this genre." App does not crash or show a blank screen.  
**Actual Result:** Typed "Romance" in the search bar — logcat showed the API was called with `genres=Romance` but no results loaded and no empty state message appeared. Screen remained blank with no feedback to the user. App did not crash.  
**Status:** ❌ Fail — BUG-012 (no empty state handling)

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
1. Turn off WiFi on the emulator
2. Open the app
3. Navigate to genre search
4. Type any genre or tap CATEGORIES

**Expected Result:** App displays a user-friendly error message such as "No internet connection." App does not crash or freeze.  
**Actual Result:** App showed toast error message "Failed to fetch manga: Unable to resolve host 'mangaverse-api.p.rapidapi.com'". App did not crash. However the error message is technical and not user-friendly. Genre search screen showed no results and no specific error message for that screen.  
**Status:** ✅ Pass (error handled, no crash — technical message noted, see BUG-003)

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
1. Select a genre from CATEGORIES
2. Observe the screen immediately after selecting before results load

**Expected Result:** A loading indicator such as a spinner or progress bar is visible while results are being fetched from the API.  
**Actual Result:** A loading spinner was briefly visible on the home screen while manga results were being fetched after returning from categories. Loading state was present but brief. No dedicated loading indicator on the genre results screen itself.  
**Status:** ✅ Pass (loading indicator present on home screen)

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
1. Select Genre A from CATEGORIES (e.g. Action) and wait for results
2. Go back and select Genre B (e.g. Fantasy)
3. Wait for results and compare

**Expected Result:** Results update correctly to show Genre B manga. No results from Genre A remain. App does not crash.  
**Actual Result:** App navigated back correctly each time a genre was selected. No crashes. However results did not change between genres — same manga titles appeared for both Action and Fantasy confirming BUG-012. Back navigation itself worked correctly.  
**Status:** ❌ Fail — BUG-012 (navigation works, results do not change)

---

## Test Summary

| Test Case ID | Description | Status | Bugs Linked |
|---|---|---|---|
| TC-GS-001 | Select a valid genre — list loads | ✅ Pass | — |
| TC-GS-002 | Genre results match API data | ❌ Fail | BUG-012 |
| TC-GS-003 | Genre with no results — empty state shown | ❌ Fail | BUG-012 |
| TC-GS-004 | Genre search with no internet | ✅ Pass | BUG-003 |
| TC-GS-005 | Loading state while fetching results | ✅ Pass | — |
| TC-GS-006 | Switch between different genres | ❌ Fail | BUG-012 |

**Pass Rate: 3/6 (50%)**

---

> Testing conducted on Android Studio Emulator — Medium Phone API 34.  
> All bugs linked above are documented in full in bugs-found.md.
