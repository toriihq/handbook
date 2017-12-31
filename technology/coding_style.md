# Coding Style

## Standard JS

Coding style tends to be hard to agree on and leads to a lot of bikeshedding. We decided to outsource our decisions to the [standard](https://standardjs.com/) JS coding style. It has nothing standard but its name, but it aligns everyone on the same coding style.

It is used as a plugin to your favorite IDE (vi, WebStorm, vscode) and runs on every commit via a git-commit hook.

Hopefully, code reviews will never be about coding style, but making the code simple and robust.

## Guidelines

Not strict, but following these will help keep the codebase aligned:

**Prefer const over let**

Always use `const`, unless the value/reference needs to change - then use `let`. Never use `var`.

```js
// Less of this
let x = 5

// More of this
const x = 5
```

A `const` is a reference and can be used if mutating objects/arrays:

```js
// Less of this
let x = []
x.push(5)

// More of this
const x = []
x.push(5) // this is okay
x = [5] // this throws

```

**Prefer async/await over direct Promises / Callbacks**

```js
// Less of this
doSomething()
  .then(result => {
    console.log('This is the result', result)
  })

// More of this
const result = await doSomething()
console.log('This is the result', result)
```

For catching errors, use `try/catch`. Try to minimize `try/catch` blocks by capturing errors at the top most level:

```js
// Less of this
doSomething
  .then(result => {
    console.log('This is the result', result)
  })
  .catch(error => {
    console.error('This is an error', error)
  })

// More of this
try {
  const result = await doSomething()
  console.log('This is the result', result)
} catch (error) {
  console.error('This is an error', error)
}
```

**Use ES6 import/export syntax**

```js
// Less of this
const moment = require('moment')

const getDate = () => moment()

module.exports = getDate

// More of this
import moment from 'moment'

const getDate = () => moment()

export default getDate
```
