# Styling

## CSS-in-JS

Forget everything you know about separating Markup and Style. CSS-in-JS comes to solve a few problems of CSS:

- Instead of using limited compilers like SASS and LESS, using JS has all the language feature needed.
- Sharing variables from CSS to JS
- Scoping styles
- Naming classes, ids, etc...
- Refactoring and finding dead styles
- Sharing styles via npm

## Styled Components

We use [Styled Components](https://styled-components.com/) for styling. Use the Styled Components `ThemeProvider` theme for colors, sizes and other design tokens.

### Example

```jsx
import styled from 'styled-components'

const Header = styled.div`
  font-size: ${({ theme }) => theme.fontSizes.small};
  color: ${({ theme }) => theme.colors.blue};
`

return (
  <div>
    <Header>Header</Header>
  </div>
)
```

### Legacy Variables

Older code imports directly from `colors.js`, `sizes.js`, `texts.js` and `mixins.js`. When touching these files, migrate to using the theme instead.

## Legacy: Glamor

There is still [Glamor](https://github.com/threepointone/glamor) CSS in the codebase. When touching files that use Glamor, convert them to Styled Components.
