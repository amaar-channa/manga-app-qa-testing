# Test Plan — MangaMania Android App

**Project:** MangaMania  
**Version:** 1.0  
**Tester:** Amaar Yasir Channa  
**Platform:** Android  
**Date:** March 2026  
**Status:** In Progress  

---

## 1. Introduction

This test plan outlines the testing strategy, scope, tools, and schedule 
for manual QA testing of the MangaMania Android application. MangaMania 
is a manga reading app built by a team of 4 developers as a Capstone 
Project at Fanshawe College.

The goal of this test plan is to ensure all features function correctly, 
edge cases are handled gracefully, the app is stable under various network 
conditions, and the API integration works as expected.

---

## 2. Objectives

- Verify all core features function as intended
- Identify and document bugs with clear reproduction steps
- Validate that API data displayed in the app matches actual API responses
- Ensure the app handles no internet and slow internet scenarios gracefully
- Confirm that user data persists correctly across app restarts
- Verify UI consistency across different screen sizes

---

## 3. Scope

### In Scope
- Bookmark feature
- Dark Mode feature
- Search by Genre feature
- Latest Updates feature
- General app navigation and behaviour
- API testing via Postman
- Delete Data feature
- Interactive Tutorial

### Out of Scope
- Performance load testing
- Automated testing (planned for future)
- iOS version of the app
- Backend server testing

---

## 4. Test Approach

### 4.1 Manual Testing
All test cases will be executed manually on the Android Studio Emulator. 
Each test case will be run at least once and results will be documented 
as Pass or Fail with actual results noted.

### 4.2 Negative Testing
Each feature will be tested with invalid inputs, no internet connection, 
and unexpected user behaviour to ensure the app handles errors gracefully.

### 4.3 Integration Testing
API responses will be verified directly in Postman and compared against 
what the app displays to ensure data integrity.

### 4.4 UI Testing
The app will be tested on at least two different screen sizes using 
Android Studio emulator profiles to verify layout consistency.

---

## 5. Test Environment

| Item | Details |
|---|---|
| **Device** | Android Studio Emulator |
| **Android Version** | Android 13 and above |
| **Emulator Profiles** | Pixel 4 (small), Pixel 7 Pro (large) |
| **Network Conditions** | Normal, Slow (throttled), No internet |
| **API Tool** | Postman Desktop |
| **Bug Tracker** | Jira |
| **Language** | Kotlin |

---

## 6. Features to be Tested

| Feature | Test File | Test Cases |
|---|---|---|
| Bookmark | test-cases/bookmark-tests.md | 8 |
| Dark Mode | test-cases/dark-mode-tests.md | 6 |
| Search by Genre | test-cases/genre-search-tests.md | 6 |
| Latest Updates | test-cases/latest-updates-tests.md | 5 |
| General App | test-cases/general-app-tests.md | 8 |
| API Testing | test-cases/api-tests.md | 7 |
| **Total** | | **40** |

---

## 7. Bug Reporting Process

All bugs found during testing will be:
1. Documented in `bug-reports/bugs-found.md`
2. Logged in Jira with appropriate severity and priority
3. Assigned a unique Bug ID (BUG-001, BUG-002 etc.)
4. Supported with screenshots where possible

### Severity Levels
| Severity | Meaning |
|---|---|
| **Critical** | App crashes or data loss occurs |
| **High** | Major feature is broken or unusable |
| **Medium** | Feature works but behaves incorrectly |
| **Low** | Minor UI or cosmetic issue |

---

## 8. Entry and Exit Criteria

### Entry Criteria (Testing can begin when)
- App is installed and running on emulator
- All test cases are written and reviewed
- Postman is set up with API keys
- Jira project is created for bug tracking

### Exit Criteria (Testing is complete when)
- All 40 test cases have been executed
- All bugs are documented with reproduction steps
- All Critical and High severity bugs are flagged
- Test summary is updated in README

---

## 9. Risks and Assumptions

| Risk | Mitigation |
|---|---|
| RapidAPI free tier rate limits may block requests | Space out API test calls, use free tier carefully |
| Emulator behaviour may differ from real device | Note any emulator-specific observations |
| App may depend on live API data that changes | Document API responses at time of testing |
| Some features may require specific data to test | Set up test data before beginning test session |

---

## 10. Deliverables

- [x] Test Plan (this document)
- [ ] Bookmark test cases — executed and results filled
- [ ] Dark Mode test cases — executed and results filled
- [ ] Genre Search test cases — executed and results filled
- [ ] Latest Updates test cases — executed and results filled
- [ ] General App test cases — executed and results filled
- [ ] API test cases — executed and results filled
- [ ] Bug reports — documented with screenshots
- [ ] Jira board — bugs logged and tracked
- [ ] README — test summary table updated with final results

---

## 11. Test Schedule

| Task | Target Date |
|---|---|
| Test plan and test cases written | March 2026 |
| Manual testing session | March - April 2026 |
| Bug reports documented | April 2026 |
| Jira board updated | April 2026 |
| Final test summary updated | April 2026 |
