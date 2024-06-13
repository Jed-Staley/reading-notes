# Recursive Functions

## Overview

Recursive functions are a way of looping that is, in some cases, more efficient or more code-dense than a for or while loop. This is because for and while loops do not take in parameters - the closest comparison is the `i` value of the for loop, which can be useful if used as an index but is limited.

What sets recursion apart is that it is a method of looping that takes in a parameter. If you were to write a recursive function that iterated through items in an array, each item would call the function on the next index. In this way, you end up with a chain of function calls. Once that chain reaches the last link (which is when the function is run on the last item in the array), it returns instead of calling itself again. This causes a reverse effect - now, that return iterates back to the beginning of the chain, until the first function call makes its return.

## Example

Suppose a recursive function that adds the items in an array

```javascript
function addArr(item, array) {
  // finds the index of the item in the provided array
  const index = array.indexOf(item);

  // checks to see if the item is the last item in the provided array
  if (index === array.length - 1) {
    // if so, it returns the item unchanged
    return item;
  } else {
    // if not, it returns the item added to the function run on the next item in the array
    return item + addArr(array[index + 1], array);
  }
}
```

If we wanted the sum of an array, we would get it like this:

```javascript
const arr = [2, 6, 64, 8, 3, 85, 23, 76];

const sum = addArr(arr[0], arr);
```

This inputs `2` as the first argument since `2` is the first item in the array. Since this is not the last item in the array, it runs the line:

```javascript
return item + addArr(array[index + 1], array);
```

We know that `item` is `2`, but what is `addArr(array[index + 1], array)`? Well, that function is run as a result.

Now we run the function on the next item in the array, which runs the function on the next item, and so on. Eventually, we reach the end and find that the item `76` has an index which is equal to the array's length - 1. So, instead of calling the function again, this function call returns `76`.

Now, the return statements start going *back* up the chain. The previous function call was on the 7th item, item `23`. In that function call, we ran the same line that we ran for the first function call:

```javascript
return item + addArr(array[index + 1], array);
```

Before, `item` was equal to `2`, but now, `item` is equal to `23`. But what is `addArr(array[index + 1], array)`? Well, we just found that out. Running `addArr()` on the last item in the function returned `76`. So now, we find that the return for the next to last item is `23 + 76` which is `99`. And this will be the return for the `addArr()` that was called on the previous item.

This will continue back up the line until we reach the first item, where we initally found that the sum was `2` + `addArr(array[index + 1], array)`. Now, we know that that addArr() function call will evaluate to the sum of all the other numbers in the array. First `76 + 23`, then `85 + 99`, then `3 + 184`, and so on all the way to `265`. So the first function call resolves to `267`, which is the sum of the array.

## Conclusion

This is not a great use case for recursion - it would be much easier to simply use a for loop. But in other data structures, the only way to get to the next item is *through the previous item*. In this example, we used these lines to get the next item:

```javascript
const index = array.indexOf(item);
array[index + 1]
```

But in a linked list for example, the next item is simply `node.next`. This makes recursion a very efficient way of accessing the data in a linked list. Furthermore, in B-Trees, depending on what your algorithm is doing, you may need to access every single node in the tree, and they're not all in a simple line like an array! In cases like this, recursion can be used so that everytime a function is called on a leaf node, it simply returns, and starts a return chain back up to the closest node that has other children, meaning every node only has to be visited once. This is immensly more efficient than starting from the root node and starting over every single time you reach a leaf node.
