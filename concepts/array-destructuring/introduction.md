# Introduction

JavaScript's array destructuring syntax is a concise way to extract values from an array and assign them to distinct variables.

In this example, each value in the `numberOfMoons` array is assigned to its corresponding planet:

```javascript
const numberOfMoons = [0, 2, 14];
const [venus, mars, neptune] = numberOfMoons;

neptune;
// => 14
```
This way you can reach to the value through the variable created.

You don't need to set a variable to each element in the array. Instead you can group the elements in only one variable using `...` before the variable name, this way every element that was not set to an variable will be stored in this one as a new array.

```javascript
const fruitsBasket = [orange, pear, pineapple, apple]
const [fruit1, ...otherFruits] = fruitsBasket

console.log(fruit1)
console.log(...otherFruits)
// => orange
// => ['pear', 'pineapple', 'apple']
```

You can ignore array itens by using `,` instead of naming variables in the destructured array. We ca do this using the same array example above:

```javascript
const [fruit1, , , ...otherFruits] = fruitsBasket

console.log(fruit1)
console.log(...otherFruits)
// => orange
// => apple
```

It is important to notice that after you set a variable to one of the array elements, you'll still need to separete it from the ignored elements using a `,`, therefore the first comma after you desestructure an element still won't serve to ignore elements of the array.
