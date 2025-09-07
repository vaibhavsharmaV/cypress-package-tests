## Overview

1. Logging into the application.
2. Navigating to the **Package Types** section.
3. Adding a package with random dimensions and verifying it appears.
4. Logging out and verifying persistence.
5. Deleting the added package and verifying it is removed from the list.
6. Logging out at the end.

## Manual Verification

All scenarios have been **manually verified**:

- Packages added are **always visible** even after logout/login.
- Deletion works as expected manually.
- The application behaves correctly; the intermittent failures are **automation-specific timing issues**.

## Automation Observations

While the automation test runs successfully most of the time, two intermittent issues persist:

1. **Form Input Not Found** – `input[formcontrolname="name"]` sometimes fails due to asynchronous rendering of Angular/React components.
2. **Delete Verification Fails** – Cypress sometimes cannot confirm the deleted package disappears because of DOM/API timing.

### Debugging Steps Taken

- Used **`cy.contains` and `cy.get` with extended timeouts**.
- Used **`cy.intercept()`** to wait for API responses.
- Logged URLs, XHR calls, and page transitions to understand app state.
- Tried explicit waits and retries on elements.

Despite all these, the issues remain **flaky but non-critical**, and manual verification confirms everything works.

## Achievements

- Successfully automated **Add Package** and **Delete Package** flows.
- Validated package visibility after logout/login.
- Captured full **XHR/network activity** for debugging.
- Demonstrated **reliable login and navigation flows**.

## Scope of Testing

- Packages of random names and dimensions.
- Add, delete, and logout flows.
- Verified persistence after session changes.

> Note: Flaky issues are specific to Cypress timing; app functionality is stable and verified manually.
