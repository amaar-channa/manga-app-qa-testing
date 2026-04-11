# manga-app-qa-testing
Manual QA testing documentation, test cases and bug reports for MangaMania Android app

# MangaMania — QA Test Documentation

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Platform](https://img.shields.io/badge/Platform-Android-green)
![Language](https://img.shields.io/badge/Language-Kotlin-purple)

## About This Repository

This repository contains manual QA testing documentation for **MangaMania**,
an Android manga reading application built by a team of 4 developers 
as a Capstone Project at Fanshawe College.

It includes a full test plan, manual test cases, bug reports, 
and API testing performed using Postman.

---

## About the App

MangaMania is an Android app that allows manga enthusiasts to read, 
browse, and discover manga comics on the go.

**Original Repository:** [nishu1998/Capstone_Project](https://github.com/nishu1998/Capstone_Project)  
**Platform:** Android  
**Language:** Kotlin  
**API Source:** MangaVerse API & Best Manga Anime Wallpapers API (RapidAPI)  
**App Built:** May 17 – August 9, 2024  
**QA Testing:** March–April 2026

---

## About the App — Important Note

The MangaVerse API free tier has content availability limitations. Some manga
chapter IDs tested return 404 responses at time of QA testing. The reading
feature was confirmed working during active development (May–August 2024,
verified via recorded demo). Test results reflect current API state as of
March–April 2026.

---

## My Role

**Developer:** Amaar Yasir Channa  
**Features I Built:**
- Bookmark — save and manage favourite manga
- Dark Mode — toggle for low light reading
- Latest Updates — display newest manga releases
- Search by Genre — filter manga by genre selection

**QA Role:**  
Designed and executed the full test plan for the application, 
including manual test cases, negative testing, edge case testing, 
and API endpoint verification.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Jira | Bug tracking and test management |
| Postman | API endpoint testing |
| Android Studio Emulator | Test execution environment |
| Chrome DevTools | Network and console inspection |
| Git / GitHub | Version control |

---

## Test Coverage Summary

| Area | Test Cases | Pass | Fail | Blocked | Bugs Found |
|---|---|---|---|---|---|
| Bookmark Feature | 8 | 4 | 2 | 2 | 4 (BUG-001 to BUG-004) |
| Dark Mode | 6 | 5 | 1 | 0 | 4 (BUG-005 to BUG-008) |
| Search by Genre | 6 | 3 | 3 | 0 | 1 (BUG-012) |
| Latest Updates | 5 | 4 | 0 | 1 | 1 (BUG-013) |
| General App / Navigation | 8 | 6 | 2 | 0 | 4 (BUG-003, BUG-004, BUG-014, BUG-015) |
| API Testing (Postman) | 5 | TBD | TBD | TBD | TBD |
| **Total** | **38** | **22** | **8** | **3** | **15** |

> Note: BUG-003 and BUG-004 were originally found during feature testing but are reflected in General App counts. BUG-009 and BUG-010 relate to the Read feature and are not attributed to a separate test section.

---

## Repository Structure
```
manga-app-qa-testing/
│
├── README.md                   
├── test-plan.md                
├── test-cases/
│   ├── bookmark-tests.md       
│   ├── dark-mode-tests.md      
│   ├── genre-search-tests.md   
│   ├── latest-updates-tests.md 
│   ├── general-app-tests.md    
│   └── api-tests.md            
├── bug-reports/
│   └── bugs-found.md           
├── postman/
│   └── mangamania-api.json     
└── screenshots/
    └── jira-board.png          
```

---

## Current Progress

- [x] Test plan written
- [x] Bookmark test cases complete — 8 cases, 4 pass / 2 fail / 2 blocked
- [x] Dark mode test cases complete — 6 cases, 5 pass / 1 fail
- [x] Genre search test cases complete — 6 cases, 3 pass / 3 fail
- [x] Latest updates test cases complete — 5 cases, 4 pass / 1 deferred
- [x] General app test cases complete — 8 cases, 6 pass / 2 fail
- [ ] API tests complete in Postman
- [x] Bug reports documented — 15 bugs (BUG-001 to BUG-015)
- [ ] Jira board set up
- [ ] ISTQB Foundation — in progress

---

## Key Test Scenarios

### Bookmark Feature
- Bookmark a manga and verify it appears in saved list
- Bookmark the same manga twice — check for duplicates
- Remove a bookmark — verify immediate removal
- Verify bookmarks persist after app restart
- Bookmark with no internet connection

### Dark Mode
- Toggle dark mode on — verify full UI switch
- Toggle off — verify complete revert
- Verify dark mode preference saves after restart
- Check readability of manga images in dark mode
- Verify splash screen reflects dark mode setting
- Toggle dark mode while reading a chapter

### Search by Genre
- Select a valid genre — verify relevant results load
- Select genre with no results — verify empty state message
- Test with no internet — verify error handling
- Verify API response matches displayed results

### Latest Updates
- Verify latest manga loads on home screen
- Tap a manga from latest updates — verify correct detail screen opens
- Test with no internet — verify error handling
- Verify loading state is visible while fetching

### General App / Navigation
- Verify app launches within acceptable time
- Test back button navigation across all screens
- Verify app handles slow and no internet gracefully
- Test tutorial on first launch
- Verify UI consistency across different screen sizes
- Test dark mode and bookmark features in combination

### API Testing
- Verify MangaVerse API returns 200 OK
- Test invalid genre parameter — check error response
- Verify wallpaper API response structure
- Check response time baseline
- Verify data displayed in app matches API response

---

## Bugs by Severity

| Severity | Count | Bug IDs |
|---|---|---|
| Critical | 1 | BUG-009 |
| High | 7 | BUG-001, BUG-002, BUG-004, BUG-005, BUG-007, BUG-010, BUG-012 |
| Medium | 4 | BUG-003, BUG-006, BUG-014, BUG-015 |
| Low | 3 | BUG-008, BUG-011, BUG-013 |
| **Total** | **15** | |

---

## About the Developer

**Amaar Yasir Channa**  
Mobile Application Development Graduate — Fanshawe College  
GitHub: [amaar-channa](https://github.com/amaar-channa)  
Location: London, ON, Canada
