# ESLint

[ESLint](https://eslint.org/) is a tool to lint Javascript code, and using special rules it can lint Angular projects.

## How to use it

* Install the ESLint package using npm.
```
$ npm install eslint --save-dev
```
* Copy and paste the following code inside your `.eslintrc.json` file
```javascript
{
  "parserOptions": {
    "ecmaVersion": 6,
    "sourceType": "module"
  },
  "env": {
    "browser": true,
    "angular/mocks": true,
    "es6": true
  },
  "plugins": [ "angular" ],
  "globals": {
    "moment": true
  },
  "extends": [
    "eslint:recommended",
    "angular"
  ],
  "rules": {
    "quotes": [ 2, "single" ],
    "no-unused-labels": "off",
    "prefer-const": "warn",
    "no-trailing-spaces": "warn",
    "no-continue": "warn",
    "no-var": "warn",
    "sort-vars": "warn",
    "arrow-body-style": ["warn", "as-needed"],
    "arrow-spacing": "warn",
    "no-confusing-arrow": "warn",
    "prefer-template": "warn",
    "keyword-spacing": "warn",
    "angular/on-watch": "warn",
    "angular/controller-as": "warn",
    "angular/no-service-method": "warn",
    "angular/no-services": "warn",
    "angular/controller-as-vm": [ 2, "$ctrl" ],
    "angular/di": [
      1,
      "array",
      { "matchNames": false }
    ]
  },
  "settings":{
    "angular": 1
  }
}
```

* Execute `eslint` and review the output.
