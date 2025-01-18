# Silent Failure in Expo AsyncStorage with Large Data

This repository demonstrates a bug in Expo's AsyncStorage where storing large amounts of data silently fails without throwing any error messages. This makes debugging and identifying the issue particularly challenging.

## Bug Description
When attempting to store a large JSON object exceeding AsyncStorage's storage limits, the operation appears to complete without errors. However, the data is not actually stored, leading to unexpected app behavior.

## Reproduction Steps
1. Clone this repository.
2. Run the `bug.js` file.
3. Observe the lack of error messages despite data storage failure.

## Solution
The `bugSolution.js` file provides a solution that implements data chunking to handle large data, ensuring it is stored properly.