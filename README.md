# Restful Booker API testing

Test artifacts for the Restful Booker assignment.

## Contents

- `restful-booker.postman_collection.json` — ordered CRUD collection with assertions.
- `test-cases.xlsx` — 33 positive, negative, and boundary test cases.
- `bug-reports.xlsx` — four defects reproduced on 2026-10-01.

## Run

Import the collection into Postman and run the collection in folder order. No environment is required: variables are stored at collection level. The collection creates its own booking, uses only that ID for update/delete checks, and deletes it at the end. The public service periodically resets data and can be slow, so an isolated transport timeout should be rerun before it is reported as a product defect.

Default credentials are taken from the public API documentation. Do not commit real credentials or generated tokens.

## Evidence

The bug reports are based on direct calls to the public service. RB-001 was reproduced twice, including after a two-second delay. The temporary valid booking used for verification was deleted after the check.
