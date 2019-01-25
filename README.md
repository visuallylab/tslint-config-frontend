# tslint-config-frontend
Lint rules related to web frontend development using React

# Prerequisite
1. tslint
2. typescript
3. prettier

# Usage
Follow these steps to use the rules in tslint, and enable the pre-commit hook.
1. Install the package
```
npm install --save-dev @visuallylab/tslint-config-frontend lint-staged husky
```
or
```
yarn add --dev @visuallylab/tslint-config-frontend lint-staged husky
```
2. Add config in tslint.json
```
{
  "extends": "@visuallylab/tslint-config-frontend"
}
```
3. Add configs to the package.json of your project
```
{
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "*.{ts,tsx,js,json,css,md}": ["prettier --write", "git add"]
  },
  "prettier": {
  "singleQuote": true,
  "jsxSingleQuote": false
  }
}
``` 