# @patrtorg/eligendi-eius
Helpers to handle array operations in a more elegant way

## Instalation
```sh
npm i @patrtorg/eligendi-eius
```

## Helper Functions

* flat10

### flat10

This function flattens an array, hence the name flat10 (flatten), do you get it?

```js
const {flat10} = require('@patrtorg/eligendi-eius');
// or
// const {flat10} = require('@patrtorg/eligendi-eius/flat10');

const arrayInput = [1, [2, [3, [4], [5], [6, 7]]], [8, [9]]];

const arrayOutput = flat10(arrayInput);

console.log(arrayOutput); // [1, 2, 3, 4, 5, 6, 7, 8, 9]
```
You can read the test code in [test/flat10.test.js](test/flat10.test.js) for more examples.

### inChunks

```js
const {inChunks} = require('@patrtorg/eligendi-eius');

const arrayInput = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15];
const CHUNK_SIZE = 5
// Split in chunks of 5 elements each
const arrayOutput = inChunks(arrayInput, CHUNK_SIZE);

console.log(arrayOutput); // [ [ 1, 2, 3, 4, 5 ], [ 6, 7, 8, 9, 10 ], [ 11, 12, 13, 14, 15 ] ]
```