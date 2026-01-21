## Array Swap Utility

A simple data manipulation function designed to transpose the positions of two elements with an array.

### The Logic

While there are many ways to swap values in JavaScript, the `.reverse()` method is uniquely suited for this specific constraint (exactly two values).

    1. In-Place Mutation: The `.reverse()` method modifies the original array and returns it.

    2. Two-Point Transposition: In a two-element array, the "reverse" operation effectively swaps index `0` with index `1`.

### Alternative: Destructuring

If you wanted to do this without mutating the original array, or if you were swapping specific variables, modern JavaScript offers **Destructuring Assignment**:

```JavaScript

function arraySwap(arr) {
    // Swapping using array destructuring
    let [a, b] = arr;
    return [b, a];
}

```

### What I Learned

1. Built-in Method Efficiency

I learned that for simple tasks like flipping a two-item list, I don't need to manually create a `temp` variable. Leveraging JavaScript's built-in `Array.prototype.reverse()` makes the code more concise.

2. Mutation vs Returning

I practiced returning the result og a method directly. However, I also learned that `.reverse()` is **destructive**, meaning it changes the original array. If I needed to keep the original array "A, B" intact somewhere, I might use a non-destructive method like `[...arr].reverse()`.

3. Structural Flexibility

I reinforced the idea that an array is just an ordered list of pointers. Swapping them is simply a matter of reordering those pointers, whether through a reverse algorithm or a destructuring assignment.
