1. Construct a function intersection that compares input arrays and returns a new array with elements found in all of the inputs. You can only use reduce method to do this.

```js
function intersection(...arrays) {
  let first = arrays[0];
  let second = arrays[1];
  let finalArr = [];
  let final;

  let result = first.reduce((acc, cv) => {
    if (second.includes(cv)) {
      acc = acc.concat(cv);
    }
    return acc;
  }, []);

  for (i = 2; i < arrays.length; i++) {
    final = result.reduce((acc, cv) => {
      if (arrays[i].includes(cv)) {
        acc = acc.concat(cv);
      }
      return acc;
    }, []);
  }
  return final;
}

or;

// function intersection(...arrays){
//   return arrays.reduce((acc,cv)=>{
//     acc = acc.filter(elm => cv.includes(elm));
//     return acc;
//   })
// }

// Test
console.log(
  intersection([5, 10, 15, 20], [15, 88, 1, 5, 7], [1, 10, 15, 5, 20])
); // should log: [5, 15]
```

2. Construct a function `union` that compares input arrays and returns a new array that contains all elements. If there are duplicate elements, only add it once to the new array. Preserve the order of the elements starting from the first element of the first input array. You can only use reduce method to do this.

```js
function union(...arrays) {
  let first = arrays[0];
  let second = arrays[1];
  let finalArr = [];
  let final;

  let result = second.reduce((acc, cv) => {
    if (!first.includes(cv)) {
      acc = acc.concat(cv);
    }
    return acc;
  }, first);

  for (i = 2; i < arrays.length; i++) {
    final = arrays[i].reduce((acc, cv) => {
      if (!result.includes(cv)) {
        acc = result.concat(cv);
      }
      return acc;
    }, result);
  }
  return final;
}

// function intersection(...arrays){
//   return arrays.reduce((acc,cv)=>{
//     acc = acc.filter(elm => !cv.includes(elm)).concat(cv);
//     return acc;
//   })
// }

// Test
console.log(union([5, 10, 15], [15, 88, 1, 5, 7], [100, 15, 10, 1, 5]));
// should log: [5, 10, 15, 88, 1, 7, 100]
```
