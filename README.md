# Standard [Preact](https://preactjs.com/) - ESLint Shareable Config

[![Greenkeeper badge](https://badges.greenkeeper.io/zouhir/eslint-config-standard-preact.svg)](https://greenkeeper.io/)
[![travis][travis-image]][travis-url]
[![npm][npm-image]][npm-url]
[![downloads][downloads-image]][downloads-url]

[travis-image]: https://travis-ci.org/zouhir/eslint-config-standard-preact.svg?branch=master
[travis-url]: https://travis-ci.org/zouhir/eslint-config-standard-preact
[npm-image]: https://img.shields.io/npm/v/eslint-config-standard-preact.svg
[npm-url]: https://npmjs.org/package/eslint-config-standard-preact
[downloads-image]: https://img.shields.io/npm/dm/eslint-config-standard-preact.svg
[downloads-url]: https://npmjs.org/package/eslint-config-standard-preact

#### An ESLint [Shareable Config](http://eslint.org/docs/developer-guide/shareable-configs) for Preact/JSX support in [JavaScript Standard Style](https://github.com/feross/standard).

## Install

```bash
npm install eslint-config-standard-preact
```

## Usage

Shareable configs are designed to work with the `extends` feature of `.eslintrc` files.
You can learn more about
[Shareable Configs](http://eslint.org/docs/developer-guide/shareable-configs) on the
official ESLint website.

This Shareable Config adds React and JSX to the baseline JavaScript Standard Style rules
provided in `eslint-config-standard`.

##### Here's how to install everything you need:

```bash
npm install --save-dev eslint-config-standard eslint-config-standard-preact eslint-plugin-promise eslint-plugin-react eslint-plugin-standard
```

Then, add this to your .eslintrc file:

```
{
  "extends": ["standard", "standard-preact"]
}
```

*Note: We omitted the `eslint-config-` prefix since it is automatically assumed by ESLint.*

## New Linting Features

```js
{/* class property name is now allowed in JSX as well as className */}
<div class='container' /> ✅
```

```js
export default class App extends Component {
  handleRoute = e => { // ✅ You can assign to an ES6 class method
    this.currentUrl = e.url;
  }
}
```

```js
// no need to have React linter and then this line in every file
/** @jsx h */ 🗑
```

## Override Settings

You can override settings from the shareable config by adding them directly into your
`.eslintrc` file. 

#### Looking for something easier than this?

The easiest way to use JavaScript Standard Style to check your code is to use the
[`standard`](https://github.com/feross/standard) package. This comes with a global
Node command line program (`standard`) that you can run or add to your `npm test` script
to quickly check your style.

## Badge

Use this in one of your projects? Include one of these badges in your readme to
let people know that your code is using the standard style.

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

```markdown
[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)
```

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](https://github.com/feross/standard)

```markdown
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](https://github.com/feross/standard)
```


## Learn more

For the full listing of rules, editor plugins, FAQs, and more, visit the main
[JavaScript Standard Style repo](https://github.com/feross/standard).

## Credit

This module is a fork of [feross/eslint-config-standard-react](https://github.com/feross/eslint-config-standard-react)

## License

MIT