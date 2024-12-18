# MongoDB Aggregation: Handling Missing or Non-Numeric Data in $avg

This example demonstrates a subtle issue in MongoDB aggregation pipelines when using the `$avg` operator. The `$avg` operator silently returns `null` when encountering non-numeric values or missing fields, which can lead to unexpected results and make debugging difficult.

The `bug.js` file contains an aggregation pipeline that calculates the average age of users grouped by city.  The pipeline will produce incorrect results if any `age` field is missing or contains non-numeric data. The `bugSolution.js` file demonstrates a way to filter out these invalid entries before calculating the average.

This bug highlights the importance of data validation and handling edge cases in MongoDB aggregation pipelines.