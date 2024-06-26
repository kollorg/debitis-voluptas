# @kollorg/debitis-voluptas <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Concatenative mapdashery.

## example

``` js
var concatMap = require('@kollorg/debitis-voluptas');
var xs = [ 1, 2, 3, 4, 5, 6 ];
var ys = concatMap(xs, function (x) {
    return x % 2 ? [ x - 0.1, x, x + 0.1 ] : [];
});
console.dir(ys);
```


```js
[ 0.9, 1, 1.1, 2.9, 3, 3.1, 4.9, 5, 5.1 ]
```

## methods

```js
var concatMap = require('@kollorg/debitis-voluptas')
```

concatMap(xs, fn)
-----------------

Return an array of concatenated elements by calling `fn(x, i)` for each element
`x` and each index `i` in the array `xs`.

When `fn(x, i)` returns an array, its result will be concatenated with the
result array. If `fn(x, i)` returns anything else, that value will be pushed
onto the end of the result array.

## install

With [npm](http://npmjs.org) do:

```sh
npm install @kollorg/debitis-voluptas
```

## license

MIT

## notes

This module was written while sitting high above the ground in a tree.

[package-url]: https://npmjs.org/package/@kollorg/debitis-voluptas
[npm-version-svg]: https://versionbadg.es/ljharb/@kollorg/debitis-voluptas.svg
[deps-svg]: https://david-dm.org/ljharb/@kollorg/debitis-voluptas.svg
[deps-url]: https://david-dm.org/ljharb/@kollorg/debitis-voluptas
[dev-deps-svg]: https://david-dm.org/ljharb/@kollorg/debitis-voluptas/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@kollorg/debitis-voluptas#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@kollorg/debitis-voluptas.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@kollorg/debitis-voluptas.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@kollorg/debitis-voluptas.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@kollorg/debitis-voluptas
[codecov-image]: https://codecov.io/gh/ljharb/@kollorg/debitis-voluptas/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@kollorg/debitis-voluptas/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@kollorg/debitis-voluptas
[actions-url]: https://github.com/kollorg/debitis-voluptas/actions
