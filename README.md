# saucedemo-qa-testing

Manual QA project for the SauceDemo e-commerce site (https://www.saucedemo.com): a test plan, 56 designed test cases (smoke, negative, boundary) and documented defects.

**Status:** In progress. 38 of 56 test cases executed, 4 defects logged. Checkout and Navigation modules are still to run.

## What's inside

| Folder | Contents |
|---|---|
| [`docs/`](docs) | [Test plan](docs/TEST_PLAN.md) |
| [`test-cases/`](test-cases) | [Test cases and execution results](test-cases/saucedemo-test-cases.xlsx) |
| [`bug-reports/`](bug-reports) | One markdown file per defect |
| [`evidences/`](evidences) | Screenshots supporting the bug reports |

## Scope

Login and logout, product list and sorting, cart, checkout, and menu/footer navigation. See the test plan for what is out of scope.

## Results so far

| Module | Test cases | Executed | Passed | Failed |
|---|---|---|---|---|
| Login | 15 | 15 | 15 | 0 |
| Product list | 10 | 10 | 10 | 0 |
| Cart | 12 | 12 | 10 | 2 |
| Checkout | 14 | 1 | 1 | 0 |
| Navigation | 5 | 0 | 0 | 0 |
| **Total** | **56** | **38** | **36** | **2** |

The smoke suite (9 cases) has been executed, and all 9 passed.

## Defects logged

| ID | Summary | Severity | Priority |
|---|---|---|---|
| [BUG-001](bug-reports/BUG-001.md) | Checkout can be completed with an empty cart | Major | High |
| [BUG-002](bug-reports/BUG-002.md) | Three products cannot be added to the cart as problem_user | Major | Medium |
| [BUG-003](bug-reports/BUG-003.md) | Remove button on the Products page does not work as problem_user | Major | Medium |
| [BUG-004](bug-reports/BUG-004.md) | All products show the same incorrect image as problem_user | Minor | High |

## Approach

- **Techniques:** equivalence partitioning, boundary value analysis, error guessing
- **Test types:** smoke, functional, negative, boundary, regression, exploratory
- **Process:** run the smoke suite first, execute the remaining cases module by module, log each defect with steps and evidence, then summarize results

## Tools

Microsoft Excel / Google Sheets · Markdown · Git and GitHub · VS Code · Chrome DevTools

## Next

Key smoke cases are being automated with Playwright and JavaScript in a separate repository, [saucedemo-playwright-automation](https://github.com/DellZaragosa/saucedemo-playwright-automation), with each automated test linked back to its manual case ID.

## Author

Wendell Zaragosa