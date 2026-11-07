# saucedemo-qa-testing

Manual QA project for the SauceDemo e-commerce site (https://www.saucedemo.com): a test plan, 56 designed test cases (smoke, negative, boundary) and documented defects.

**Status:** in progress. Plan and test cases are written; execution and defect logging are under way.

## What's inside

| Folder | Contents |
|---|---|
| [`docs/`](docs) | [Test plan](docs/TEST_PLAN.md) |
| [`test-cases/`](test-cases) | [Test cases and execution results](test-cases/saucedemo-test-cases.xlsx) |
| `bug-reports/` | One markdown file per defect (added as bugs are found) |
| `evidence/` | Screenshots supporting test results and bug reports |

## Scope

Login and logout, product list and sorting, cart, checkout, and menu/footer navigation. See the test plan for what is out of scope.

| Module | Test cases |
|---|---|
| Login | 15 |
| Product list | 10 |
| Cart | 12 |
| Checkout | 14 |
| Navigation | 5 |
| **Total** | **56** (9 smoke) |

## Approach

- **Techniques:** equivalence partitioning, boundary value analysis, error guessing
- **Test types:** smoke, functional, negative, boundary, regression, exploratory
- **Process:** run the smoke suite first, execute the remaining cases module by module, log each defect with steps and evidence, then summarize results

## Results

_To be added after execution: cases executed, passed, failed, blocked, and defects logged._

## Tools

Microsoft Excel / Google Sheets · Markdown · Git and GitHub · VS Code · Chrome DevTools

## Next

Key smoke cases will be automated with Playwright and JavaScript in a separate repository, `saucedemo-playwright-automation`, with each automated test linked back to its manual case ID.

## Author

Wendell Zaragosa · www.linkedin.com/in/zaragosawendell/