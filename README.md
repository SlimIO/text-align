# text-align
![version](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/SlimIO/text-align/master/package.json&query=$.version&label=Version)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/SlimIO/text-align/commit-activity)
![MIT](https://img.shields.io/github/license/mashape/apistatus.svg)
![dep](https://img.shields.io/david/SlimIO/text-align)
![size](https://img.shields.io/github/repo-size/SlimIO/text-align)
![known vulnerabilities](https://img.shields.io/snyk/vulnerabilities/github/SlimIO/text-align)
[![Build Status](https://travis-ci.com/SlimIO/text-align.svg?branch=master)](https://travis-ci.com/SlimIO/text-align)

A wide-character aware text alignment function for use in terminals / on the console. This package is a modern implementation of [wide-align](https://github.com/iarna/wide-align) with String.prototype.padLeft and String.prototype.padRight.

## Requirements
- [Node.js](https://nodejs.org/en/) v12 or higher

## Getting Started

This package is available in the Node Package Repository and can be easily installed with [npm](https://docs.npmjs.com/getting-started/what-is-npm) or [yarn](https://yarnpkg.com).

```bash
$ npm i @slimio/text-align
# or
$ yarn add @slimio/text-align
```

### Usage example

```js
const align = require("@slimio/text-align");

console.log(align.center('abc', 10));     // '   abc    '
console.log(align.center('古古古', 10));   // '  古古古  '
console.log(align.left('abc', 10));       // 'abc       '
console.log(align.left('古古古', 10));     // '古古古    '
console.log(align.right('abc', 10));      // '       abc'
console.log(align.right('古古古', 10));    // '    古古古'
```

## API

### `align.center(str: string, length: number)` → string
Returns *str* with spaces added to both sides such that that it is *length*
chars long and centered in the spaces.

### `align.left(str: string, length: number)` → string
Returns *str* with spaces to the right such that it is *length* chars long.

### `align.right(str: string, length: number)` → string
Returns *str* with spaces to the left such that it is *length* chars long.

## Dependencies

|Name|Refactoring|Security Risk|Usage|
|---|---|---|---|
|[@slimio/wcwidth](https://github.com/SlimIO/wcwidth)|Minor|Low|Determine columns needed for a fixed-size wide-character string|

## License
MIT
