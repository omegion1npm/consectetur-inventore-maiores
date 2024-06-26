# @omegion1npm/consectetur-inventore-maiores <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Robustly `.call.bind()` a function.

## Getting started

```sh
npm install --save @omegion1npm/consectetur-inventore-maiores
```

## Usage/Examples

```js
const assert = require('assert');
const callBind = require('@omegion1npm/consectetur-inventore-maiores');
const callBound = require('@omegion1npm/consectetur-inventore-maiores/callBound');

function f(a, b) {
	assert.equal(this, 1);
	assert.equal(a, 2);
	assert.equal(b, 3);
	assert.equal(arguments.length, 2);
}

const fBound = callBind(f);

const slice = callBound('Array.prototype.slice');

delete Function.prototype.call;
delete Function.prototype.bind;

fBound(1, 2, 3);

assert.deepEqual(slice([1, 2, 3, 4], 1, -1), [2, 3]);
```

## Tests

Clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@omegion1npm/consectetur-inventore-maiores
[npm-version-svg]: https://versionbadg.es/ljharb/@omegion1npm/consectetur-inventore-maiores.svg
[deps-svg]: https://david-dm.org/ljharb/@omegion1npm/consectetur-inventore-maiores.svg
[deps-url]: https://david-dm.org/ljharb/@omegion1npm/consectetur-inventore-maiores
[dev-deps-svg]: https://david-dm.org/ljharb/@omegion1npm/consectetur-inventore-maiores/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@omegion1npm/consectetur-inventore-maiores#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@omegion1npm/consectetur-inventore-maiores.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@omegion1npm/consectetur-inventore-maiores.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@omegion1npm/consectetur-inventore-maiores.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@omegion1npm/consectetur-inventore-maiores
[codecov-image]: https://codecov.io/gh/ljharb/@omegion1npm/consectetur-inventore-maiores/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@omegion1npm/consectetur-inventore-maiores/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@omegion1npm/consectetur-inventore-maiores
[actions-url]: https://github.com/omegion1npm/consectetur-inventore-maiores/actions
