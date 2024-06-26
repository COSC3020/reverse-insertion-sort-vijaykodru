[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Bi-S25fM)
# Reverse Insertion Sort

Consider the code for insertion sort we covered in class:

```javascript
function insertionSort(arr) {
  for(var i = 1; i < arr.length; i++) {
    var val = arr[i];
    var j;
    for(j = i; j > 0 && arr[j-1] > val; j--) {
      arr[j] = arr[j-1];
    }
    arr[j] = val;
  }
  return arr;
}
```

Change this function such that it works from the end of the array rather than
the beginning, `insertionSortReverse()` -- only the direction of
iterating over the elements is reversed, the array is still sorted the same way
(ascending). Add your code in `code.js`. Test your new function; I've provided
some basic testing code that uses [jsverify](https://jsverify.github.io/) in
`code.test.js`.

## Average-Case Time Complexity of Insertion Sort

In the lectures, we covered that insertion sort has best-case time complexity of
$\Theta(n)$ and worst-case time complexity of $\Theta(n^2)$. What is the
average-case time complexity ($\Theta$)?

Hint: Think about what happens in each iteration of the loop, and how often the
loop is executed. Keep in mind that for asymptotic analysis we don't care about
constant factors.

Describe your reasoning and the conclusion you've come to. Your reasoning is
most important -- you can easily find the answer, but you need to demonstrate
that you've understood the concept. Add your answer to this markdown file.

Lets consider a time complexity being $\Theta{(n)}$ this means that the given is array is sorted already and the outer loop would go through every element not swaping anything making this the best case.

if we consider a time complexity being $\Theta{(n^2)}$ this means that the array is reverse sorted which requires the outer loop to go through n elements and swapping them n times making this the worst case.

And finally, when it comes to average case time complexity, we will be assuming the given array is roughly sorted half way. This would require the outer loop go through n elements swapping them at the most n/2 times. So the time complexity would be $\Theta{(n^2/2)}$. Asymtotically we can neglect the constants as they do not effect the runtime. So the average time complexity of the insertion sort is also $\Theta{(n^2)}$

Reference: 
Lecture slides
Geeks for geeks
