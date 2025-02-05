# MongoDB $inc Operator Error
This repository demonstrates an uncommon error related to the usage of the `$inc` operator in MongoDB update queries.

The error occurs when using a string value instead of a number with the `$inc` operator. This leads to unexpected behavior and prevents the correct incrementation of the counter field.

## Bug Description
The bug involves incorrect usage of the `$inc` operator within a MongoDB update operation. The `$inc` operator is designed to increment a numerical value, but when provided with a string, MongoDB interprets it differently, resulting in incorrect update behavior.

## Solution
The solution involves ensuring the value passed to `$inc` is a number (integer or float) rather than a string.  This corrects the update operation and results in the expected behavior. 

## How to Reproduce
1.  Clone the repository.
2. Connect to your MongoDB instance.
3. Run the `bug.js` script. Observe the incorrect update result.
4. Run the `bugSolution.js` script. Observe the correct update result.