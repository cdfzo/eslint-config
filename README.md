# cdfzo/eslint-config

My personal ESLint configuration for TypeScript projects.

## Usage

Edit `eslint.config.js`:

```js
import config from '@cdfzo/eslint-config'

export default [config]
```

Make sure your `.prettierrc` looks like this:

```json
{
  "semi": false,
  "singleQuote": true
}
```

## Override Rules

Have a look at the documentation for
[eslint](https://eslint.org/docs/latest/rules/) and
[typescript-eslint](https://typescript-eslint.io/rules/).

You can override rules like this:

```js
export default [
  config,
  rules: {
    '@typescript-eslint/array-type': 0,
    'max-lines': 0,
  }
]
```

## Note

This package already includes `eslint`, `@typescript-eslint/eslint-plugin` and
`@typescript-eslint/parser`. You don't need to install them separately.
