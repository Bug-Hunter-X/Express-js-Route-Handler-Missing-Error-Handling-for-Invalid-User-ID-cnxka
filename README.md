# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without validating it, leading to a potential crash if the ID is not a number.  The solution shows how to add proper input validation and error handling to prevent crashes.

## Bug

The `bug.js` file shows the buggy code. The `parseInt` function is used without checking for `NaN` which could crash the application if the request parameter is not a number.

## Solution

The `bugSolution.js` file shows the corrected code with input validation and error handling added to prevent the crash.  It checks if the parsed ID is NaN before attempting to use it. 