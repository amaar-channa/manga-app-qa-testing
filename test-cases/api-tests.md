# API Testing — Test Cases

**Feature:** API Testing via Postman  
**Platform:** Android / Postman  
**Tested On:** Postman Desktop  
**Date:** March 2026  
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
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

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
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

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
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

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
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

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
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

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
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

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
**Actual Result:** [ To be filled during testing ]  
**Status:** [ Pass / Fail ]

---

## Test Summary

| Test Case ID | Description | Status |
|---|---|---|
| TC-API-001 | MangaVerse API returns 200 OK | Pending |
| TC-API-002 | MangaVerse API genre filter | Pending |
| TC-API-003 | Invalid genre parameter | Pending |
| TC-API-004 | API response time | Pending |
| TC-API-005 | Wallpaper API returns valid data | Pending |
| TC-API-006 | API request with invalid key | Pending |
| TC-API-007 | App data matches API response | Pending |
