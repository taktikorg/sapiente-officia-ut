# @taktikorg/sapiente-officia-ut <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Object-related atoms: Object, ToObject, RequireObjectCoercible.

## Example

```js
const assert = require('assert');

const $Object = require('@taktikorg/sapiente-officia-ut');
const ToObject = require('@taktikorg/sapiente-officia-ut/ToObject');
const RequireObjectCoercible = require('@taktikorg/sapiente-officia-ut/RequireObjectCoercible');

assert.equal($Object, Object);
assert.throws(() => ToObject(null), TypeError);
assert.throws(() => ToObject(undefined), TypeError);
assert.throws(() => RequireObjectCoercible(null), TypeError);
assert.throws(() => RequireObjectCoercible(undefined), TypeError);

assert.deepEqual(RequireObjectCoercible(true), true);
assert.deepEqual(ToObject(true), Object(true));

const obj = {};
assert.equal(RequireObjectCoercible(obj), obj);
assert.equal(ToObject(obj), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@taktikorg/sapiente-officia-ut
[npm-version-svg]: https://versionbadg.es/ljharb/@taktikorg/sapiente-officia-ut.svg
[deps-svg]: https://david-dm.org/ljharb/@taktikorg/sapiente-officia-ut.svg
[deps-url]: https://david-dm.org/ljharb/@taktikorg/sapiente-officia-ut
[dev-deps-svg]: https://david-dm.org/ljharb/@taktikorg/sapiente-officia-ut/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@taktikorg/sapiente-officia-ut#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikorg/sapiente-officia-ut.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/sapiente-officia-ut.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/es-object.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/sapiente-officia-ut
[codecov-image]: https://codecov.io/gh/ljharb/@taktikorg/sapiente-officia-ut/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@taktikorg/sapiente-officia-ut/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@taktikorg/sapiente-officia-ut
[actions-url]: https://github.com/taktikorg/sapiente-officia-ut/actions
