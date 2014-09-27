# Ember-cli-accounting

This is a port of the great [accounting.js](https://github.com/openexchangerates/accounting.js) library to
ES6 modules that integrates seamlessly with ember-cli.

## Instalation

Just add like any other ember-cli addon:

`npm install ember-cli-accounting --save-dev`

## Usage

You no longer need to access the global accounting, you can import only what you need:

```js
import formatMoney from "accounting/format-money"
```

Althoug you can import everything as expected:

```js
import accounting from "accounting"
```

## Differences with accounting.js

Although this is almost a 1:1 port of accountant.js, there is a few differences:

* Each function of accountant.js lives in its own module, so you can only import those functions you want to use.
* Removed polifills for things like Array.prototype.map. Since this is going to be used with ember, we can
give for granted that those functions will be there.
* More tests than the original.

## Versioning

At the time of writting, this addon bundles the same funcionality than accounting version 0.4.1.
This addon's version don't match accounting's version. However, you can check accounting's version easily:

```js
import version from "accounting/version";

console.log(version) // => "0.4.1"
```

## Documentation

This library does not make any change in the public api of accounting.js, so you can read the official
documentation [here](http://openexchangerates.github.io/accounting.js/)