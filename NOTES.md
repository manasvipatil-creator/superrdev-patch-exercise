# NOTES

## Summary of Changes
- Fixed the SQL search condition by grouping the title and description search with parentheses.
- Reset pagination to the first page when the search query or status filter changes.
- Prevented stale API responses from updating the UI by ignoring outdated requests in the custom hook.
- Removed the artificial delay from the backend controller.
- Updated the Oracle SQL reference to match the repository query.

## What I Chose Not to Change
I did not change the sorting order because the project consistently uses `ORDER BY created_at DESC`, and there was no documented requirement to use ascending order.

## Biggest Remaining Risk
The application loads all matching records before applying pagination. This approach may not scale well for larger datasets and database-level pagination would be more efficient.

## AI / Tools Used
I used ChatGPT and Antigravity IDE to help analyze the codebase, identify potential bugs, review fixes, and validate changes. I manually reviewed the suggestions, selected the fixes to apply, and tested the application after making the changes.