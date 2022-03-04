## Task 1: displaying output

One function which does both data processing and also renders UI is often doing too many things.

### What to do
Reorganize the given function into two functions, one to perform the processing **and** one to perform the UI rendering.

#### Step 1

Let's assume you are writing e-commerce software such as [Shopify](https://www.shopify.com/), so you deal with orders.

First, write code to do this:

```
// Define the Order object, if your language requires this.
// Add a few plausible fields, the level of realism is up to you.

function printAverageOrderValue(orders) {
	// Reduce orders to an integer of average order value in cents,
    // rounded down to the closest cent.

	// Print this amount to the UI console.
}
```

Commit this to git with a self-explanatory commit subject, e.g., `Implement printing average order value.`

#### Step 2
Consider how to write a test of this function. (Don't actually do it yet.)

Hmm, how to test console output?

A bit difficult, isn't it?

#### Step 3

Rewrite the code to separate the calculation from the printing (i.e., introduce a new function).

#### Step 4

Write a unit test of the function that now performs only pure calculation.

A lot easier, isn't it?

Commit this to git with a self-explanatory commit subject, e.g., `Refactor to separate calculation from printing, and add a unit test.`

