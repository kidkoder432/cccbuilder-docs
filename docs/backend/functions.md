---
title: Functions
nav_order: 1
parent: CCCBuilder Backend

---
# Lambda Functions

CCCBuilder uses only one Lambda function to handle all requests. However, the function's URL actually has three endpoints, which each perofrm a separate function:

- `/primary`: This endpoint fetches the ASSIST articulations from a user's primary CCC to the user's intended universities and majors and returns both articulated courses (with all available articulation options) and non-articulated courses.
- `/whitelist`: This endpoint checks the provided set of courses against the user's intended universities and majors and returns the university courses that have been articulated.
- `/template`: This endpoint parses the `templateAssets` object from an ASSIST agreement and repackages the required courses, including special instructions on competing a given number of courses or credits from a set, into a more accessible form for the frontend.
