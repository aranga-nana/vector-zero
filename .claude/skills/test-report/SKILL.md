---
name: test-report
description: Record a test, its measurements and its pass/fail result for a Vector-Zero project in test-results/. Use when the owner ran a test (range, battery life, current draw, flight test, sensor accuracy, thermal, endurance) or wants to plan one.
---

# Test report

1. Identify the project and the question the test answers. If the test hasn't happened yet, write the plan: goal, pass criteria, setup and procedure. Set the result to `PLANNED`.
2. Write `test-results/<project>/YYYY-MM-DD-<test-slug>.md` from `_templates/test-report.md`.
3. Record the setup precisely: hardware revision, firmware version or commit, tools, and environment. Put the numbers in the results table, with units. Save raw logs next to the report.
4. Give an honest result. A failed test is valuable: record why it failed and what changes.
5. For drone or high-power tests, note the safety steps: props off for bench tests, failsafe checked, battery checked, legal flying area.
6. Link the report from the project README. Update the risk assessment if a risk was retired or a new one appeared.
7. Reply with the result, what it means for the project, and the next test.
