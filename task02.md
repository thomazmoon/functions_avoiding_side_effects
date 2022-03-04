### Task 2: modifying a member of a passed-in array

Let's say a function accepts an array of values.

If the function changes the elements of this passed-in array, this fact is not obvious from outside the function.

I.e., doing so creates a side-effect, there is a result of calling this function that isn't discernible just by inspecting the function's return value.

Functions whose return values fully represent the result are easier to reason about.

### What to do

Reorganize the given function such that a new array is returned.

This way, what the function does is completely understood just from the return value.

#### Step 1

Let's assume you are writing flashcard study software such as [Anki](https://www.ankiapp.com/).

Your function will receive a deck of flashcards, and based on some simple [spaced repetition algorithm](https://en.wikipedia.org/wiki/Spaced_repetition), it will mark a future time when each card should be presented for review.

1. First, write code to do this:

```
// Define the Deck and Card objects, if your language requires this.
// Add a few plausible fields, the level of realism is up to you.

function markReviewTimes(deck) {
    // for each card
        // calculate the next-review datetime based on some criteria of your choice  
            // (i.e. if correct show tomorrow, else show up again in 10 minutes)
        // update the card to record this value
    // return the deck, or nothing (your choice)
}
```

2. Unit test the above.
3. Commit this to git with a self-explanatory commit subject, e.g., `Implement marking card next-review times.`

#### Step 2

1. Factor out the next-review-time calculation into its own function.
2. Unit test the factored-out function.
3. Commit this to git with a self-explanatory commit subject.

#### Step 3

1. Change the `markReviewTimes()` function to create a new copy of the deck of flashcards.
2. It is your choice whether to make a [deep copy or a shallow copy](https://www.cs.utexas.edu/~scottm/cs307/handouts/deepCopying.htm).
3. Think about the difference and document the reason for your choice in the function comment of `markReviewTimes()`.
4. Return the new deck.
5. Don't forget to update your unit tests.
6. Commit this to git.

