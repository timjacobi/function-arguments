# [function-arguments][author-www-url] [![npmjs.com][npmjs-img]][npmjs-url] [![The MIT License][license-img]][license-url] 

> Get arguments of a function, useful for and used in dependency injectors. Works for regular functions, generator functions and arrow functions.

[![code climate][codeclimate-img]][codeclimate-url] [![standard code style][standard-img]][standard-url] [![travis build status][travis-img]][travis-url] [![coverage status][coveralls-img]][coveralls-url] [![dependency status][david-img]][david-url]

## Install
```
npm i function-arguments --save
```

## Usage
> For more use-cases see the [tests](./test.js)

```js
const functionArguments = require('function-arguments')
```

### [functionArguments](index.js#L33)
> Get function arguments names.

**Params**

* `fn` **{Function}**: Function from which to get arguments names.    
* `returns` **{Array}**  

**Example**

```js
var fnArgs = require('function-arguments')

console.log(fnArgs(function (a, b, c) {})) // => [ 'a', 'b', 'c' ]
console.log(fnArgs(function named (a , b, c) {})) // => [ 'a', 'b', 'c' ]

console.log(fnArgs(a => {})) // => [ 'a' ]
console.log(fnArgs((a, b) => {})) // => [ 'a', 'b' ]

console.log(fnArgs(function * (a ,b, c) {})) // => [ 'a', 'b', 'c' ]
console.log(fnArgs(function * named (a ,b, c) {})) // => [ 'a', 'b', 'c' ]
```

### Works when using comments
> As it works for ES2015, it also works if you use comments in weird places.

```js
console.log(fnArgs(function /* something may */ (
  // go,
  go,
  /* wrong, */
  here
  // (when, using, comments) {}
) { return 1 })) // => [ 'go', 'here' ]
```

## Related
* [flatten-arguments](https://www.npmjs.com/package/flatten-arguments): Fastest, simplest and smallest. Pass `arguments` object or list… [more](https://www.npmjs.com/package/flatten-arguments) | [homepage](https://github.com/tunnckocore/flatten-arguments)
* [fn-args](https://www.npmjs.com/package/fn-args): Get the arguments of a function | [homepage](https://github.com/sindresorhus/fn-args)
* [fn-name](https://www.npmjs.com/package/fn-name): Get the name of a named function | [homepage](https://github.com/sindresorhus/fn-name)
* [get-fn-name](https://www.npmjs.com/package/get-fn-name): Get function name with strictness and correctness in mind.… [more](https://www.npmjs.com/package/get-fn-name) | [homepage](https://github.com/tunnckocore/get-fn-name)
* [handle-arguments](https://www.npmjs.com/package/handle-arguments): Handles given Arguments object - return separatly last argument… [more](https://www.npmjs.com/package/handle-arguments) | [homepage](https://github.com/hybridables/handle-arguments)
* [manage-arguments](https://www.npmjs.com/package/manage-arguments): Prevents arguments leakage - managing arguments. From Optimization killers… [more](https://www.npmjs.com/package/manage-arguments) | [homepage](https://github.com/tunnckocore/manage-arguments)
* [parse-function](https://www.npmjs.com/package/parse-function): Parse a function, arrow function or string to object… [more](https://www.npmjs.com/package/parse-function) | [homepage](https://github.com/tunnckocore/parse-function)

## Contributing
Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/tunnckoCore/function-arguments/issues/new).  
But before doing anything, please read the [CONTRIBUTING.md](./CONTRIBUTING.md) guidelines.

## [Charlike Make Reagent](http://j.mp/1stW47C) [![new message to charlike][new-message-img]][new-message-url] [![freenode #charlike][freenode-img]][freenode-url]

[![tunnckoCore.tk][author-www-img]][author-www-url] [![keybase tunnckoCore][keybase-img]][keybase-url] [![tunnckoCore npm][author-npm-img]][author-npm-url] [![tunnckoCore twitter][author-twitter-img]][author-twitter-url] [![tunnckoCore github][author-github-img]][author-github-url]

[arr-map]: https://github.com/jonschlinkert/arr-map
[is-number]: https://github.com/jonschlinkert/is-number

[npmjs-url]: https://www.npmjs.com/package/function-arguments
[npmjs-img]: https://img.shields.io/npm/v/function-arguments.svg?label=function-arguments

[license-url]: https://github.com/tunnckoCore/function-arguments/blob/master/LICENSE
[license-img]: https://img.shields.io/badge/license-MIT-blue.svg

[codeclimate-url]: https://codeclimate.com/github/tunnckoCore/function-arguments
[codeclimate-img]: https://img.shields.io/codeclimate/github/tunnckoCore/function-arguments.svg

[travis-url]: https://travis-ci.org/tunnckoCore/function-arguments
[travis-img]: https://img.shields.io/travis/tunnckoCore/function-arguments/master.svg

[coveralls-url]: https://coveralls.io/r/tunnckoCore/function-arguments
[coveralls-img]: https://img.shields.io/coveralls/tunnckoCore/function-arguments.svg

[david-url]: https://david-dm.org/tunnckoCore/function-arguments
[david-img]: https://img.shields.io/david/tunnckoCore/function-arguments.svg

[standard-url]: https://github.com/feross/standard
[standard-img]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg

[author-www-url]: http://www.tunnckocore.tk
[author-www-img]: https://img.shields.io/badge/www-tunnckocore.tk-fe7d37.svg

[keybase-url]: https://keybase.io/tunnckocore
[keybase-img]: https://img.shields.io/badge/keybase-tunnckocore-8a7967.svg

[author-npm-url]: https://www.npmjs.com/~tunnckocore
[author-npm-img]: https://img.shields.io/badge/npm-~tunnckocore-cb3837.svg

[author-twitter-url]: https://twitter.com/tunnckoCore
[author-twitter-img]: https://img.shields.io/badge/twitter-@tunnckoCore-55acee.svg

[author-github-url]: https://github.com/tunnckoCore
[author-github-img]: https://img.shields.io/badge/github-@tunnckoCore-4183c4.svg

[freenode-url]: http://webchat.freenode.net/?channels=charlike
[freenode-img]: https://img.shields.io/badge/freenode-%23charlike-5654a4.svg

[new-message-url]: https://github.com/tunnckoCore/ama
[new-message-img]: https://img.shields.io/badge/ask%20me-anything-green.svg

