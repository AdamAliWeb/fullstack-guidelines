# JavaScript

## References

- **[JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript)**

- **[Regular Expressions Syntax Reference Sheet](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Regular_expressions/Cheatsheet)**

### Libraries

---

## Tips & Tricks

1. Avoid using `eval()` in your code as it can reduce performance and pose a security risk by granting excessive privileges to evaluated text.

2. Prefer using `===` over `==` because `===` checks both the value and data type, whereas `==` only checks the value.

3. It's better to use new array methods like `array.toSorted()` and `array.toReversed()` for array manipulation instead of `array.reverse()` or `array.sort()`. This is because new methods create a copy of the array, while the old ones modify the original array, potentially disrupting the original order.

4. - You can swap the values of two variables using destructuring:

   ```js
   let a = 8;
   let b = 6;

   [a, b] = [b, a];

   // a = 6
   // b = 8
   ```

5. Ways to copy arrays

   ```js
   //normal arrays
   let arr = [1, 2, 3];
   let arrCopy = [...arr];

   arrCopy.push(4);

   // arr = [1, 2, 3]
   // arrCopy = [1, 2, 3, 4]

   //multidimensional arrays
   let arr2 = [[1, 2], [3]];
   let arrCopy2 = arr.map((item) => item.slice());

   arrCopy[1].push(4);

   // arr = [[1, 2], [3]]
   // arrCopy2 = [[1, 2], [3, 4]]
   ```
