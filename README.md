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

| Area | Test Cases | Bugs Found |
|---|---|---|
| Bookmark Feature | 8 | TBD |
| Dark Mode | 6 | TBD |
| Search by Genre | 6 | TBD |
| Latest Updates | 5 | TBD |
| General App / Navigation | 8 | TBD |
| API Testing (Postman) | 5 | TBD |
| **Total** | **38** | **TBD** |

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

- [ ] Test plan written
- [ ] Bookmark test cases complete
- [ ] Dark mode test cases complete
- [ ] Genre search test cases complete
- [ ] Latest updates test cases complete
- [ ] General app test cases complete
- [ ] API tests complete in Postman
- [ ] Bug reports documented
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

### Search by Genre
- Select a valid genre — verify relevant results load
- Select genre with no results — verify empty state message
- Test with no internet — verify error handling
- Verify API response matches displayed results

### API Testing
- Verify MangaVerse API returns 200 OK
- Test invalid genre parameter — check error response
- Verify wallpaper API response structure
- Check response time baseline
- Verify data displayed in app matches API response

---

## About the Developer

**Amaar Yasir Channa**  
Mobile Application Development Graduate — Fanshawe College  
GitHub: [amaar-channa](https://github.com/amaar-channa)  
Location: London, ON, Canada
