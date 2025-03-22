# overview

The code in thie project is based on the book named "Programming TypeScript: Making Your JavaScript Applications Scale (Japanese Edition)"

## setup ESLint for TypeScript

### create .eslintrc.js

```bash
npm install --save-dev typescript eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser

touch .eslintrc.js
```

.eslintrc.js

```javascript
module.exports = {
  root: true,
  parser: '@typescript-eslint/parser',
  parserOptions: {
    project: './tsconfig.json'
  },
  plugins: [
    '@typescript-eslint'
  ],
  extends: [
    'eslint:recommended',
    'plugin:@typescript-eslint/eslint-recommended',
    'plugin:@typescript-eslint/recommended',
    'plugin:@typescript-eslint/recommended-requiring-type-checking'
  ]
}
```

### run lint

```bash
npx eslint . --ext ts
```
