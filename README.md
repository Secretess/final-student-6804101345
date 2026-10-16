# Playwright Software Testing Final

Automated tests for [SauceDemo](https://www.saucedemo.com/) using Playwright Test and TypeScript.

## Setup and run

```powershell
npm install
npx playwright install chromium
npx playwright test
```

The test run writes an HTML report to `playwright-report/` and a JSON report to `reports/results.json`. Open the HTML report with:

```powershell
npx playwright show-report
```

## Test coverage

- `UT-01`: login validation for empty credentials, missing password, and invalid credentials.
- `UT-02`: Backpack add/remove button state and cart badge.
- `IT-01`: performs a real SauceDemo login, then replaces the page DOM with an inventory stub using `page.setContent()`. The login and inventory URL are real; the mock inventory DOM and its two products are stubbed.
- `IT-02`: a driver adds the `session-username=standard_user` cookie and opens the real inventory URL directly. The inventory, cart behavior, and cart contents are real SauceDemo UI; only the login state is prepared by the driver.
- `ST-01`: completes a purchase of Backpack and Bike Light.
- `ST-02`: checks required checkout fields, recovers with valid information, and completes a purchase.

## Reports

After running the suite, see `reports/test-summary.md` for the run summary and `reports/results.json` plus `playwright-report/` for the generated reports.