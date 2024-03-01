# JS - frequently used function:

### **1. `splice` (Array Method)**

- **Parameters**: **`start`**, **`deleteCount`** (optional), **`...items`** (optional)
- **Return Value**: An array containing the deleted elements.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3, 4];
    arr.splice(2, 1, 'a', 'b'); // Returns [3], arr is now [1, 2, 'a', 'b', 4]
    
    ```
    

### **2. `filter` (Array Method)**

- **Parameters**: **`callback(element[, index[, array]])`**, **`thisArg`** (optional)
- **Return Value**: A new array with elements that pass the test implemented by the provided function.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let numbers = [1, 2, 3, 4];
    let even = numbers.filter(n => n % 2 === 0); // Returns [2, 4]
    
    ```
    

### **3. `map` (Array Method)**

- **Parameters**: **`callback(currentValue[, index[, array]])`**, **`thisArg`** (optional)
- **Return Value**: A new array with the results of calling a provided function on every element in the calling array.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let numbers = [1, 2, 3, 4];
    let squares = numbers.map(n => n * n); // Returns [1, 4, 9, 16]
    
    ```
    

### **4. `reduce` (Array Method)**

- **Parameters**: **`callback(accumulator, currentValue[, index[, array]])`**, **`initialValue`** (optional)
- **Return Value**: The single value that results from the reduction.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let sum = [1, 2, 3, 4].reduce((acc, val) => acc + val, 0); // Returns 10
    
    ```
    

### **5. `forEach` (Array Method)**

- **Parameters**: **`callback(currentValue [, index [, array]])`**, **`thisArg`** (optional)
- **Return Value**: **`undefined`**.
- **Example**:
    
    ```jsx
    javascriptCopy code
    [1, 2, 3, 4].forEach(alert); // Alerts each number in turn
    
    ```
    

### **6. `every` (Array Method)**

- **Parameters**: **`callback(element[, index[, array]])`**, **`thisArg`** (optional)
- **Return Value**: **`true`** if the callback function returns a truthy value for every array element; otherwise, **`false`**.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let allEven = [2, 4, 6].every(n => n % 2 === 0); // Returns true
    
    ```
    

### **7. `some` (Array Method)**

- **Parameters**: **`callback(element[, index[, array]])`**, **`thisArg`** (optional)
- **Return Value**: **`true`** if the callback function returns a truthy value for at least one element in the array; otherwise, **`false`**.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let someEven = [1, 2, 3].some(n => n % 2 === 0); // Returns true
    
    ```
    

### **8. `find` (Array Method)**

- **Parameters**: **`callback(element[, index[, array]])`**, **`thisArg`** (optional)
- **Return Value**: The value of the first element in the array that satisfies the provided testing function. Otherwise, **`undefined`**.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let found = [1, 2, 3, 4].find(n => n > 2); // Returns 3
    
    ```
    

### **9. `findIndex` (Array Method)**

- **Parameters**: **`callback(element[, index[, array]])`**, **`thisArg`** (optional)
- **Return Value**: The index of the first element in the array that satisfies the provided testing function. Otherwise, -1.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let index = [1, 2, 3, 4].findIndex(n => n > 2); // Returns 2
    
    ```
    

### **10. `sort` (Array Method)**

- **Parameters**: **`compareFunction`** (optional)
- **Return Value**: The sorted array.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [3, 1, 4, 1, 5, 9];
    arr.sort((a, b) => a - b); // Returns [1, 1, 3, 4, 5, 9]
    
    ```
    

### **11. `concat` (Array Method)**

- **Parameters**: **`...values`** (Arrays and/or values)
- **Return Value**: A new array consisting of the elements in the object on which it is called, followed in order by, for each argument, the elements of that argument (if the argument is an array) or the argument itself (if the argument is not an array).
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr1 = [1, 2, 3];
    let arr2 = [4, 5, 6];
    let combined = arr1.concat(arr2); // Returns [1, 2, 3, 4, 5, 6]
    
    ```
    

### **12. `slice` (Array Method)**

- **Parameters**: **`begin`** (optional), **`end`** (optional)
- **Return Value**: A shallow copy of a portion of an array into a new array object selected from **`begin`** to **`end`** (**`end`** not included). The original array will not be modified.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3, 4, 5];
    let sliced = arr.slice(1, 3); // Returns [2, 3]
    
    ```
    

### **13. `includes` (Array/String Method)**

- **Parameters**: **`searchElement`**, **`fromIndex`** (optional)
- **Return Value**: **`true`** if the array/string includes the element/value, **`false`** otherwise.
- **Example** (Array):
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3];
    let includesTwo = arr.includes(2); // Returns true
    
    ```
    
- **Example** (String):
    
    ```jsx
    javascriptCopy code
    let str = "hello";
    let includesEllo = str.includes("ello"); // Returns true
    
    ```
    

### **14. `indexOf` (Array/String Method)**

- **Parameters**: **`searchElement`**, **`fromIndex`** (optional)
- **Return Value**: The first index at which a given element can be found in the array/string, or -1 if it is not present.
- **Example** (Array):
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3];
    let indexOfTwo = arr.indexOf(2); // Returns 1
    
    ```
    
- **Example** (String):
    
    ```jsx
    javascriptCopy code
    let str = "hello";
    let indexOfE = str.indexOf("e"); // Returns 1
    
    ```
    

### **15. `join` (Array Method)**

- **Parameters**: **`separator`** (optional)
- **Return Value**: A string with all array elements joined. If **`separator`** is not specified, a comma (**`,`**) will be used.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3];
    let joined = arr.join("-"); // Returns "1-2-3"
    
    ```
    

### **16. `toString` (Global Object Method)**

- **Parameters**: None
- **Return Value**: A string representing the object.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let num = 123;
    let str = num.toString(); // Returns "123"
    
    ```
    

### **17. `toLocaleString` (Global Object Method)**

- **Parameters**: Varies by object
- **Return Value**: A string representing the object. This method is meant to be overridden by derived objects for locale-specific purposes.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let num = 123456.789;
    let str = num.toLocaleString('en-US'); // Returns "123,456.789" for US English locale
    
    ```
    

### **18. `shift` (Array Method)**

- **Parameters**: None
- **Return Value**: The removed element from the array; **`undefined`** if the array is empty.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3];
    let first = arr.shift(); // Returns 1, arr is now [2, 3]
    
    ```
    

### **19. `unshift` (Array Method)**

- **Parameters**: **`...elements`**
- **Return Value**: The new length of the array.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [2, 3];
    let newLength = arr.unshift(1); // Returns 3, arr is now [1, 2, 3]
    
    ```
    

### **20. `reverse` (Array Method)**

- **Parameters**: None
- **Return Value**: The reversed array.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3];
    arr.reverse(); // Now arr is [3, 2, 1]
    
    ```
    

### **21. `fill` (Array Method)**

- **Parameters**: **`value`**, **`start`** (optional), **`end`** (optional)
- **Return Value**: The modified array, filled with **`value`** from **`start`** to **`end`**.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3, 4];
    arr.fill(0, 2, 4); // Now arr is [1, 2, 0, 0]
    
    ```
    

### **22. `copyWithin` (Array Method)**

- **Parameters**: **`target`**, **`start`** (optional), **`end`** (optional)
- **Return Value**: The modified array.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3, 4, 5];
    arr.copyWithin(0, 3); // Now arr is [4, 5, 3, 4, 5]
    
    ```
    

### **23. `flat` (Array Method)**

- **Parameters**: **`depth`** (optional)
- **Return Value**: A new array with all sub-array elements concatenated into it recursively up to the specified depth.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, [2, [3, [4]]]];
    let flattened = arr.flat(2); // Returns [1, 2, 3, [4]]
    
    ```
    

### **24. `flatMap` (Array Method)**

- **Parameters**: **`callback(currentValue[, index[, array]])`**, **`thisArg`** (optional)
- **Return Value**: A new array formed by applying a given callback function to each element of the array, and then flattening the result by one level.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = [1, 2, 3];
    let mappedAndFlattened = arr.flatMap(x => [x, x * 2]); // Returns [1, 2, 2, 4, 3, 6]
    
    ```
    

### **25. `keys` (Object/Array Method)**

- **Parameters**: None
- **Return Value**: A new Array Iterator object that contains the keys for each index in the array/object.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = ['a', 'b', 'c'];
    let iterator = arr.keys();
    for (let key of iterator) {
      console.log(key); // logs 0, 1, 2
    }
    
    ```
    

### **26. `values` (Object/Array Method)**

- **Parameters**: None
- **Return Value**: A new Array Iterator object that contains the values for each index in the array/object.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = ['a', 'b', 'c'];
    let iterator = arr.values();
    for (let value of iterator) {
      console.log(value); // logs "a", "b", "c"
    }
    
    ```
    

### **27. `entries` (Object/Array Method)**

- **Parameters**: None
- **Return Value**: A new Array Iterator object that contains the [key, value] pairs for each index in the array/object.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = ['a', 'b', 'c'];
    let iterator = arr.entries();
    for (let entry of iterator) {
      console.log(entry); // logs [0, "a"], [1, "b"], [2, "c"]
    }
    
    ```
    

### **28. `from` (Array Method)**

- **Parameters**: **`arrayLike`**, **`mapFn`** (optional), **`thisArg`** (optional)
- **Return Value**: A new Array instance from an array-like or iterable object.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = Array.from("123", num => Number(num)); // Returns [1, 2, 3]
    
    ```
    

### **29. `of` (Array Method)**

- **Parameters**: **`...elements`**
- **Return Value**: A new Array instance with a variable number of elements.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let arr = Array.of(1, 2, 3); // Returns [1, 2, 3]
    
    ```
    

### **30. `isArray` (Array Method)**

- **Parameters**: **`obj`**
- **Return Value**: **`true`** if the object is an array; otherwise, **`false`**.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let isArray = Array.isArray([1, 2, 3]); // Returns true
    
    ```
    

The remaining items on your list refer to various JavaScript and Web APIs for type checking, parsing, and encoding/decoding strings. Due to the vast number of items, I'll provide a general structure for those functions without detailed examples:

### **31-47. Type Checking (Various)**

- **Example Structure**:
    
    ```jsx
    javascriptCopy code
    let isType = Type.isType(variable); // Returns true or false based on the type check
    
    ```
    

### **48-57. Parsing and String/URI Handling (Global Functions)**

- **Example Structure**:
    
    ```jsx
    javascriptCopy code
    let result = FunctionName(input[, additionalParameters]);
    
    ```
    

### **58. `eval` (Global Function)**

- **Parameters**: **`string`**
- **Return Value**: The result of executing the string as JavaScript code.
- **Example**:
    
    ```jsx
    javascriptCopy code
    let result = eval('2 + 2'); // Returns 4
    
    ```