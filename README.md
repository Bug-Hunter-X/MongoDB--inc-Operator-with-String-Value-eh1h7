# MongoDB $inc Operator with String Value

This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries. The error occurs when a string is used instead of a number as the increment value.

## Bug Description
The `$inc` operator is designed to increment a numeric field by a specified value.  If you attempt to use a string with `$inc`, it will not function as expected and will result in unexpected results.

## Bug Reproduction
1. Create a MongoDB collection named `myCollection` with a document like this: `db.myCollection.insertOne({ _id: 1, field: 0 })`
2. Run the incorrect update query shown in `bug.js`
3. The expected result is to have a document with `field: 5`, however an incorrect result will be returned.

## Solution
The solution is to use a number instead of a string when updating with the `$inc` operator.
