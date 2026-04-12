# API Testing — Test Cases

**Feature:** API Testing via Postman  
**Platform:** Android / Postman  
**Tested On:** Postman Desktop  
**Date:** April 2026  
**APIs Tested:**
- MangaVerse API — https://rapidapi.com/sagararofie/api/mangaverse-api
- Best Manga Anime Wallpapers API — https://rapidapi.com/onextech-solutions-onextech-solutions-default/api/best-manga-anime-wallpapers

---

## Test Cases

### TC-API-001 — MangaVerse API Returns 200 OK
| Field | Details |
|---|---|
| **Test Case ID** | TC-API-001 |
| **Feature** | API Testing |
| **Priority** | High |
| **Type** | Functional |
| **Tool** | Postman |
| **Precondition** | Valid RapidAPI key is available |

**Steps:**
1. Open Postman
2. Create a GET request to the MangaVerse API base endpoint
3. Add required headers including RapidAPI key
4. Send the request

**Expected Result:** API returns HTTP status 200 OK. Response body contains valid manga data in JSON format.  
**Actual Result:** API returned HTTP 200 OK in 940ms. Response body contains valid manga data in JSON format with fields: id, title, sub_title, status, thumb, summary, authors, genres, nsfw, type, total_chapter.  
**Status:** ✅ Pass

---

### TC-API-002 — MangaVerse API Genre Filter
| Field | Details |
|---|---|
| **Test Case ID** | TC-API-002 |
| **Feature** | API Testing |
| **Priority** | High |
| **Type** | Functional |
| **Tool** | Postman |
| **Precondition** | Valid RapidAPI key is available |

**Steps:**
1. Open Postman
2. Send a GET request to MangaVerse API with a valid genre parameter (e.g. genre=Action)
3. Review the response

**Expected Result:** API returns 200 OK. Response contains only manga matching the requested genre. JSON structure is valid and complete.  
**Actual Result:** API returned 200 OK in 392ms. Response contained manga data but results were not exclusively Action genre — multiple other genres appeared in results. This confirms the genre filtering behavior documented in BUG-012, where the API returns mixed genre results rather than filtering strictly by the requested genre.  
**Status:** ⚠️ Partial Pass — API responded correctly but genre filtering is not strict

---

### TC-API-003 — MangaVerse API Invalid Genre Parameter
| Field | Details |
|---|---|
| **Test Case ID** | TC-API-003 |
| **Feature** | API Testing |
| **Priority** | Medium |
| **Type** | Negative Testing |
| **Tool** | Postman |
| **Precondition** | Valid RapidAPI key is available |

**Steps:**
1. Open Postman
2. Send a GET request with an invalid genre parameter (e.g. genre=InvalidGenre123)
3. Review the response

**Expected Result:** API returns an appropriate error response such as 400 Bad Request or an empty results array. Response does not crash or return unhandled errors.  
**Actual Result:** API returned 200 OK with empty data array `{"code": 200, "data": []}` in 346ms. No crash or unhandled error occurred.  
**Status:** ✅ Pass

---

### TC-API-004 — MangaVerse API Response Time
| Field | Details |
|---|---|
| **Test Case ID** | TC-API-004 |
| **Feature** | API Testing |
| **Priority** | Medium |
| **Type** | Performance Testing |
| **Tool** | Postman |
| **Precondition** | Valid RapidAPI key is available |

**Steps:**
1. Open Postman
2. Send a GET request to the MangaVerse API
3. Check the response time shown in Postman

**Expected Result:** API responds within 2000ms (2 seconds). Response time is recorded as a performance baseline.  
**Actual Result:** API responded in 453ms, well within the 2000ms threshold. Response times across all test runs ranged from 346ms to 940ms.  
**Status:** ✅ Pass

---

### TC-API-005 — Wallpaper API Returns Valid Data
| Field | Details |
|---|---|
| **Test Case ID** | TC-API-005 |
| **Feature** | API Testing |
| **Priority** | High |
| **Type** | Functional |
| **Tool** | Postman |
| **Precondition** | Valid RapidAPI key is available |

**Steps:**
1. Open Postman
2. Send a GET request to the Best Manga Anime Wallpapers API
3. Review the response

**Expected Result:** API returns 200 OK. Response contains valid wallpaper data including image URLs. JSON structure is complete and matches what the app displays.  
**Actual Result:** API returned 404 with a Heroku "No such app" error page — the API backend is no longer hosted. However, the app still displays wallpapers by sourcing images directly from Unsplash URLs (confirmed via logcat: `Wallpaper URL: https://images.unsplash.com/...`). The Popular Wallpapers screen shows a blank white screen, likely caused by this dead API endpoint.  
**Status:** ❌ Fail — API backend is defunct

---

### TC-API-006 — API Request With Invalid Key
| Field | Details |
|---|---|
| **Test Case ID** | TC-API-006 |
| **Feature** | API Testing |
| **Priority** | High |
| **Type** | Security Testing |
| **Tool** | Postman |
| **Precondition** | An invalid or expired API key is used |

**Steps:**
1. Open Postman
2. Send a GET request to MangaVerse API with an incorrect API key
3. Review the response

**Expected Result:** API returns 401 Unauthorized or 403 Forbidden. Access is correctly denied with a clear error message.  
**Actual Result:** API correctly denied access. Returned 401 Unauthorized with message "Invalid API key. Go to https://docs.rapidapi.com/docs/keys for more info." when using an invalid key format. Also returned 403 Forbidden with "You are not subscribed to this API." for a valid-format but unauthorized key.  
**Status:** ✅ Pass

---

### TC-API-007 — App Data Matches API Response
| Field | Details |
|---|---|
| **Test Case ID** | TC-API-007 |
| **Feature** | API Testing / Integration |
| **Priority** | High |
| **Type** | Integration Testing |
| **Tool** | Postman + Android Studio Emulator |
| **Precondition** | App is running, internet is active |

**Steps:**
1. Open the app and navigate to the manga list
2. Note the title and details of the first manga shown
3. Call the MangaVerse API in Postman
4. Find the same manga in the API response
5. Compare all visible fields

**Expected Result:** Title, cover image, genre and description shown in the app exactly match the data returned by the API.  
**Actual Result:** API returned 200 OK with valid manga data in 482ms. Direct title-for-title comparison was not possible because the app uses a random page number (1–21) on each launch and a hardcoded genre query of `Harem,Fantasy,Action` (confirmed via logcat). The API JSON structure matches expected app data format — all required fields (id, title, thumb, genres, total_chapter) are present and correctly structured. Data integrity between API and app is confirmed at the structural level.  
**Status:** ⚠️ Partial Pass — API data structure matches app requirements; exact title match not verifiable due to random page selection on launch

---

## Test Summary

| Test Case ID | Description | Status |
|---|---|---|
| TC-API-001 | MangaVerse API returns 200 OK | ✅ Pass |
| TC-API-002 | MangaVerse API genre filter | ⚠️ Partial Pass |
| TC-API-003 | Invalid genre parameter | ✅ Pass |
| TC-API-004 | API response time | ✅ Pass |
| TC-API-005 | Wallpaper API returns valid data | ❌ Fail |
| TC-API-006 | API request with invalid key | ✅ Pass |
| TC-API-007 | App data matches API response | ⚠️ Partial Pass |
