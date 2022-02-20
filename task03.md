### Task 3: accessing external resources

When a function relies on a system facility such as a random-number generator or the current time, then an external input is introduced, aside from the direct function arguments.

This leads to a kind of side-effect that makes the behavior of the function more difficult to predict and test.

### What to do

Reorganize the function such that the external dependency is pushed into the function arguments explicitly, rather than implicitly pulled in by code in the function body.

This way, what the function does is completely understood just from reading the function parameters.

#### Step 1

Let's assume you are writing a time-tracking app such as [Toggl](https://toggl.com/track/).

First, write code to do this:

```
// Define the Session object if your language requires this.
// A "session" is a work session with, at minimum, a start time and end time (when completed).
// Add a few plausible fields, the level of realism is up to you.

function timeElapsed(currentSession) {
    // based on the actual current system time, return an integer of total minutes spent so far
    // rounded to the closest minute
}
```

Commit this to git with a self-explanatory commit subject, e.g., `Implement calculation of time elapsed so far in a session.`.

#### Step 2
Consider how to write a test of this function. (Don't actually do it yet.)

Hmm, how to test when system time keeps changing?

A bit difficult, isn't it.

#### Step 3

Rewrite the code to push the current time into the function as well.

Now try writing unit tests of this function.

A lot easier, isn't it?

Commit this to git with a self-explanatory commit subject, e.g., `Refactor to inject the time dependency, and add a unit test.`


