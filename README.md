![image for guide](https://source.unsplash.com/I5b0wNCiDg4)

### About

- This is a short introduction to how to do some common array manipulations in javascript.
- To clone this repo: https://github.com/grokkingcoding/super-short-guide-javascript-array-1.git

### The Guide

1. How do I insert new element into an array at a particular point in the array? An easy and quick wway is to use the .splice method in javascript for arrays.

The code snippet below is taking the entire array1 and inserting into array2 at the index specified by "n".

```
function sliceSplice(array1, array2, n) {
  array2.splice(n, 0, ...array1);
  return array2
}
```

2. So if we want to insert [4,5,6] into [1,2,3] at the last index how would we do it? Another way is to use .concat of the array method in javascript.

```
let arr1 = [1,2,3]
let arr2 = [4,5,6]
arr1 = arr1.concat(arr2)
```

we need...

```
arr1 = arr1.concat(arr2)
```

...because concat creates a new array after adding items to the existing array.

3. How about if we wanted to know at what index do we need to insert a particular m=number at in a sorted array? Can you think of a solution without looking?

```
let arr = [25,7,67, 50];
let number = 89;

const whereToInsert = (arr, number) =>
    arr.reduce((indexCounter, curr) => (number > curr ? ++indexCounter : indexCounter), 0);

```

"whereToInsert" will return the index in the array where to insert the number if the array was sorted. In our case it should insert 89 at the end of the arr.

4. How do you sort an array the easy way?

You can sort an array with the .sort method in javascript.

```
let arr = [25,7,67, 50];

arr.sort((a,b) => a-b);

```
