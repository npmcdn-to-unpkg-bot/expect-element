# expect-element

[![build status](https://img.shields.io/travis/mjackson/expect-element/master.svg?style=flat-square)](https://travis-ci.org/mjackson/expect-element)
[![npm package](https://img.shields.io/npm/v/expect-element.svg?style=flat-square)](https://www.npmjs.org/package/expect-element)

[expect-element](https://github.com/mjackson/expect-element) is an extension to [expect](https://github.com/mjackson/expect) that lets you write assertions for DOM elements.

## Installation

Using [npm](https://www.npmjs.org/):

    $ npm install expect expect-element

Then with a module bundler like [webpack](https://webpack.github.io/), use as you would anything else:

```js
// using an ES6 transpiler, like babel
import expect from 'expect'
import expectElement from 'expect-element'
expect.extend(expectElement)

// not using an ES6 transpiler
var expect = require('expect')
var expectElement = require('expect-element')
expect.extend(expectElement)
```

There is a UMD build in the npm package in the `umd` directory. Use it like:

```js
var expect = require('expect-element/umd/expect-element.min')
```

## Assertions

### toHaveAttribute

> `expect(element).toHaveAttribute(name, [value, [message]])`

Asserts the given DOM `element` has an attribute with the given `name`. If `value` is given, asserts the value of the attribute as well.

```js
expect(element).toHaveAttribute('id')
expect(element).toHaveAttribute('id', 'an-id')
```

### toNotHaveAttribute

> `expect(object).toNotHaveAttribute(name, [value, [message]])`

Asserts the given DOM `element` does not have an attribute with the given `name`. If `value` is given, asserts the value of the attribute as well.

```js
expect(element).toNotHaveAttribute('id')
expect(element).toNotHaveAttribute('id', 'an-id')
```

### toHaveAttributes

> `expect(element).toHaveAttribute(attributes, [message])`

Asserts the given DOM `element` has attributes with the names and values in `attributes`.

```js
expect(element).toHaveAttributes({
  id: 'an-id',
  'class': 'a-class'
})
```

### toNotHaveAttributes

> `expect(element).toNotHaveAttribute(attributes, [message])`

Asserts the given DOM `element` does not have attributes with the names and values in `attributes`.

```js
expect(element).toNotHaveAttributes({
  id: 'an-id',
  'class': 'a-class'
})
```

### toHaveText

> `expect(element).toHaveText(text, [message])`

Asserts the `textContent` of the given DOM `element` is `text`.

```js
expect(element).toHaveText('hello world')
```

### toNotHaveText

> `expect(element).toNotHaveText(text, [message])`

Asserts the `textContent` of the given DOM `element` is not `text`.

```js
expect(element).toNotHaveText('hello world')
```

## Issues

Please file issues on the [issue tracker on GitHub](https://github.com/mjackson/expect-element/issues).