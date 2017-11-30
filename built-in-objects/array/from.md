# Array.from()
[Added in ES6](https://www.ecma-international.org/ecma-262/6.0/#sec-array.from).

Creates a new `Array` instance from an array-like or iterable object.

## Sintax
```js
Array.from(arrayLike[, mapFn[, thisArg]])
```

**arrayLike**

An array-like or iterable object to convert to an array.

**mapFn** [optional]

Map function to call on every element of the array.

**thisArg** [optional]

Value to use as `this` when executing `mapFn`.

**Returns:**

A new `Array` instance.

## Examples
Convert `NodeList` to `Array`
```js
const divs = Array.from(document.querySelectorAll('div')); // every div on the page
```

Convert `arguments` to `Array`
```js
function foo() {
  // The arguments object is not an Array. It is similar to an Array, 
  // but doesn't have any Array properties except length.
  Array.from(arguments); 
  // [1, 2, b]
}
foo(1, 2, 'b');
```

Convert `String` to `Array`
```js
Array.from('awesome'); 
// [ 'a', 'w', 'e', 's', 'o', 'm', 'e' ]
Array.from("it's cool"); 
// [ 'i', 't', '\'', 's', ' ', 'c', 'o', 'o', 'l' ]
```

Convert `object` to `Array`
```js
// If the object has a length property, it will be used.
const obj = {length: 3};
Array.from(obj); 
// [undefined, undefined, undefined]
```

Create an `Array` containing `1` to `n` numbers
```js
Array.from({length: 5}, (item, index) => index + 1)
// [1, 2, 3, 4, 5]
```

## Links
* [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
* [Exploring ES6](http://exploringjs.com/es6/ch_core-features.html#sec_new-array-methods-core-feature)
* [davidwalsh](https://davidwalsh.name/array-from)
* [ECMAScript 2015 Language Specification](https://www.ecma-international.org/ecma-262/6.0/#sec-array.from)