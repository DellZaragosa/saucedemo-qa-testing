# Test Plan: SauceDemo Web Application

| | |
|---|---|
| **Author** | Wendell Zaragosa |
| **Date** | 2026-11-07 |
| **Version** | 1.0 |
| **Application under test** | SauceDemo, https://www.saucedemo.com |

## 1. Overview
SauceDemo is a public demo e-commerce site where a user logs in, browses products, adds items to a cart and completes a checkout. This plan describes the manual functional testing of its core purchase flow, performed as a portfolio project to practice test design, execution and defect reporting.

## 2. Objectives
- Verify that the core user flows (login, browse, cart, checkout, navigation) work as expected.
- Find and document defects with clear, reproducible reports.
- Identify a smoke suite of critical cases to automate in a later phase.

## 3. Scope

### In scope
- Login and logout
- Product list, sorting and product details
- Shopping cart
- Checkout (information, overview and completion)
- Menu and footer navigation

### Out of scope
- Performance and load testing
- Security testing beyond basic input handling
- Mobile and responsive layouts
- Cross-browser testing (one browser only)
- Accessibility testing

## 4. Test items and coverage
| Module | Planned test cases |
|---|---|
| Login | 15 |
| Product list | 10 |
| Cart | 12 |
| Checkout | 14 |
| Navigation | 5 |
| **Total** | **56** |

Of these, 9 are marked as smoke cases.

## 5. Test types and techniques
- **Types:** functional, negative, boundary, smoke, regression and exploratory testing.
- **Techniques:** equivalence partitioning, boundary value analysis and error guessing.
- Cases are written in `test-cases/saucedemo-test-cases.xlsx`, each with preconditions, steps, test data and an expected result.

## 6. Test approach
1. Run the 9 smoke cases first on each build or session.
2. If a smoke case fails, stop, retest once, then log the defect.
3. Execute the remaining cases module by module and record actual results and status.
4. Run the main flows with the `problem_user` and `performance_glitch_user` accounts to look for additional defects.
5. Log each defect using the bug report template and attach evidence.
6. Summarize results (executed, passed, failed, blocked, pass rate).

## 7. Test environment
| Item | Value |
|---|---|
| Browser | Chrome version 156.0.8078.80 |
| OS | Windows 11 |
| URL | https://www.saucedemo.com |
| Session | Private/incognito window to avoid saved state |

## 8. Test data
| Account | Purpose |
|---|---|
| `standard_user` | Main account for positive flows |
| `locked_out_user` | Locked-out login behavior |
| `problem_user` | Exploratory testing for defects |
| `performance_glitch_user` | Slow-response behavior |

Shared password: `secret_sauce` (published on the login page). Checkout details use simple values such as John / Doe / 12345, plus empty, long and unusual values for negative and boundary cases.

## 9. Entry criteria
- The application is reachable and stable.
- Test accounts can be used to log in.
- Test cases are written and reviewed.

## 10. Exit criteria
- All planned test cases have been executed or marked Blocked with a reason.
- All failures are logged as defects with evidence.
- No unreported Critical defects remain.
- The execution summary is complete.

## 11. Defect management
Defects are logged in `bug-reports/` (one markdown file per defect, using the template).

| Severity | Definition |
|---|---|
| Critical | App crashes or a core flow (such as checkout) is blocked with no workaround |
| Major | A main feature behaves wrongly but a workaround exists |
| Minor | Cosmetic or low-impact issue |

Priority (High / Medium / Low) states how soon a fix is wanted. Severity measures impact; priority measures urgency.

## 12. Risks and mitigations
| Risk | Mitigation |
|---|---|
| The demo site changes or becomes unavailable | Record the test date and keep screenshots as evidence |
| Expected results are assumed because there are no written requirements | Document assumptions and treat unclear behavior as "record and decide" |
| Intentionally buggy accounts may behave unpredictably | Reproduce each issue at least twice before logging it |
| Limited time | Run smoke cases first, then prioritize High-priority cases |

## 13. Assumptions and constraints
- There is no formal requirements document, so expected results are based on common e-commerce behavior and observed site conventions.
- Testing is done by one tester on one browser.

## 14. Deliverables
- This test plan
- Test cases with execution results (`test-cases/saucedemo-test-cases.xlsx`)
- Bug reports (`bug-reports/`)
- Evidence screenshots (`evidence/`)
- Execution summary in the project README

## 15. Schedule
| Activity | Target date |
|---|---|
| Test planning | 7 Nov 2026 |
| Test case design | 7 Nov 2026 |
| Smoke execution | 9 Nov 2026 |
| Full execution and defect logging | 10-16 Nov 2026 |
| Reporting | 17 Nov 2026 |
