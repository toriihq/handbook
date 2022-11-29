# UI Styling

## CSS-in-JS

Forget everything you know about separating Markup and Style. CSS-in-JS comes to solve a few problems of CSS:

- Instead of using limited compilers like SASS and LESS, using JS has all the language feature needed.
- Sharing variables from CSS to JS
- Scoping styles
- Naming classes, ids, etc...
- Refactoring and finding dead styles
- Sharing styles via npm

## Glamor

We chose [glamor](https://github.com/threepointone/glamor) for styling. We use the `colors` and `sizes` files for common variables:

## Variables

JavaScript allows us to define variables and common styling in files:

* `sizes.js` - Contains font-sizes, font-weights, zIndexes, etc...
* `colors.js` - Contains the Torii color scheme
* `texts.js` - Useful collection of typography
* `mixins.js` - Styling utilities

## Example

```jsx
import { css } from 'glamor`
import { fontSizes } from '../sizes`
import { colors } from '../colors`

const CSS = css({
  header: {
    fontSize: fontSize.small,
    color: colors.blue
  }
})

return (
  <div>
    <div {...CSS.header}>Header</div>
    <div className={CSS.header.toString()}>Or like this</div>
  </div>
)
```
