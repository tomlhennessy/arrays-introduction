# Arrays

* An array is a data type that contains a list of in order values surrounded in square brackets [].
* array.length returns the number of values in the array.
* Each value of an array is associated with a numerical index; the first value being at index 0.
* array.indexOf(value) is used to obtain the index of value within an array.
* .concat is used to concatenate multiple arrays.

## First and Last
Function takes an array as input, extracts the first and last elements, and returns their sum if the array length is even, or their difference if the array length is odd.

```javascript
let firstAndLast = function(array) {

    let first = array[0];
    let last = array[array.length - 1];

    // Check if the length of the array is even
    if (array.length % 2 === 0) {
        return first + last;
    } else {
        return first - last;
    }
}
```

## ThreeIncreasing
Checks if there are three consecutive elements in the array that form a sequence of increasing numbers and returns 'true' if found, otherwise it returns 'false'.

```javascript
let threeIncreasing = function(nums) {
    // Iterate through the array up to the third to last element
    for (let i = 0; i < nums.length - 2; i++) {
        // Check if three consecutive elements form a sequence of increasing numbers
        if (nums[i] + 1 === nums[i + 1] && nums[i + 1] + 1 === nums[i + 2]) {
            return true;
        }
    }
    return false;
}

console.log(threeIncreasing([2, 7, 8, 9]));                 // true
console.log(threeIncreasing([7, 2, 4, 5, 2, 1, 6]));        // false
```

## My Includes
Checks if a given target element exists in a provided array and returns 'true' if it is found, and 'false' otherwise.

```javascript
function myIncludes(arr, target) {
    for (let i = 0; i < arr.length; i++) {
        // Check to see if the current element is equal to the target element
        if (arr[i] === target) {
            return true;
        }
    }
    return false;
}
```
> The example above could also be solved with Array.includes() or Array.indexOf()


## Sum Array
Calculates and returns the sum of all elements in a given array using a 'for' loop to iterate through the array and accumulate the sum.

```javascript
function sumArray(array) {
    // Initialise a variable to store sum
    let sum = 0;

    for (let i=0; i < array.length; i++) {
        let num = array[i];
        // Add current element to running sum
        sum += num;
    }
    return sum;
}
```

## Doubler
Doubles each element in the input array and returns a new array containing the doubled values without modifying the original array.

```javascript
function doubler(numbers) {
    // Initialise empty array to store double nums
    let doubledNums = [];

    // Initialise counter variable i to 0
    let i = 0;

    while (i < numbers.length) {
        // Retrieve current number from the 'numbers' array
        let oldNum = numbers[i];

        let newNum = oldNum * 2;

        // Concatenate the new number to 'doubledNums' array
        doubledNums = doubledNums.concat(newNum);

        // Increment the counter variable i
        i += 1;
    }
    // Return array containing doubled numbers
    return doubledNums;
}
```
